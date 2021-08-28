---
description: Macht Methoden verfügbar, mit denen HTML-Seiten, die in einer Assistentenerweiterung gehostet werden, mit dem Assistenten kommunizieren können.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: WebWizardHost-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: c5bcf40a77c2f464d5277ac4823ed74a3f3c2bdd6a2114d2431684cc8b319f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967748"
---
# <a name="webwizardhost-object"></a>WebWizardHost-Objekt

Macht Methoden verfügbar, mit denen HTML-Seiten, die in einer Assistentenerweiterung gehostet werden, mit dem Assistenten kommunizieren können.

## <a name="members"></a>Member

Das **WebWizardHost-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **WebWizardHost-Objekt** verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](iwebwizardhost-cancel.md)                     | Simuliert einen Klick auf die Schaltfläche **Abbrechen.**<br/>                                                                                                                                    |
| [**FinalBack**](iwebwizardhost-finalback.md)               | Navigiert zur clientseitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.<br/>                                                                    |
| [**FinalNext**](iwebwizardhost-finalnext.md)               | Navigiert zur clientseitigen Assistentenseite, die der Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten vorhanden sind.<br/> |
| [**SetHeaderText**](iwebwizardhost-setheadertext.md)       | Legt den Titel und Untertitel fest, die im Assistentenheader angezeigt werden. Im Allgemeinen zeigt der Client den Header über dem HTML-Code und unterhalb der Titelleiste an.<br/>                    |
| [**SetWizardButtons**](iwebwizardhost-setwizardbuttons.md) | Aktualisiert die Schaltflächen **Zurück,** **Weiter** und **Fertig stellen** im Assistentenframe des Clients.<br/>                                                                                    |



 

### <a name="properties"></a>Eigenschaften

Das **WebWizardHost-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | BESCHREIBUNG                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Caption**](iwebwizardhost-caption.md)<br/>   | Lesen/Schreiben<br/> | Nicht implementiert.<br/>                              |
| [**Eigenschaft**](iwebwizardhost-property.md)<br/> | Lesen/Schreiben<br/> | Legt den aktuellen Wert einer Eigenschaft fest oder ruft sie ab.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |
| IID<br/>                      | CLSID \_ WebWizardHost<br/>                                                        |



 

 




