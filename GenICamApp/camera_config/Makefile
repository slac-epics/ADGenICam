TOP=../..
include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE

#----------------------------------------------------
# Create and install (or just install)
# databases, templates, substitutions like this

MODELS = $(wildcard ../*.env)
MODELS := $(subst .env,,$(MODELS))
MODELS := $(subst ../,,$(MODELS))

DB += $(addsuffix .db, $(MODELS))

DB_INSTALLS += $(addprefix $(TOP)/GenICamApp/camera_config/, $(addsuffix .env, $(MODELS)))
DB_INSTALLS += $(addprefix $(TOP)/GenICamApp/camera_config/, $(addsuffix .template, $(MODELS)))


#----------------------------------------------------
# If <anyname>.db template is not named <anyname>*.template add
# <anyname>_template = <templatename>

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

