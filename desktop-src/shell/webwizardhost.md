---
description: Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.
ms.assetid: 7b3690dc-2007-43a0-80a3-4a68e3c8464d
title: Webwizardhost-Objekt (Shldisp. h)
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
ms.openlocfilehash: 1fbaf53db11fda577e9e9c5384af5f7c62fe1944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959678"
---
# <a name="webwizardhost-object"></a>Webwizardhost-Objekt

Macht Methoden verfügbar, mit denen HTML-Seiten aktiviert werden, die in einer Assistenten Erweiterung gehostet werden, um mit dem Assistenten zu kommunizieren.

## <a name="members"></a>Member

Das **webwizardhost** -Objekt verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **webwizardhost** -Objekt verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                                                                        |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Abbrechen**](iwebwizardhost-cancel.md)                     | Simuliert das Klicken auf die Schaltfläche " **Abbrechen** ".<br/>                                                                                                                                    |
| [**Finalback**](iwebwizardhost-finalback.md)               | Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.<br/>                                                                    |
| [**Finalnext**](iwebwizardhost-finalnext.md)               | Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.<br/> |
| [**"Abadertext"**](iwebwizardhost-setheadertext.md)       | Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden. Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.<br/>                    |
| [**""-Schaltflächen**](iwebwizardhost-setwizardbuttons.md) | Aktualisiert die Schaltflächen **zurück**, **weiter** und **Fertig** stellen im Assistenten Rahmen des Clients.<br/>                                                                                    |



 

### <a name="properties"></a>Eigenschaften

Das **webwizardhost** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp           | BESCHREIBUNG                                              |
|:-------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Caption**](iwebwizardhost-caption.md)<br/>   | Lesen/Schreiben<br/> | Nicht implementiert.<br/>                              |
| [**Eigenschaft**](iwebwizardhost-property.md)<br/> | Lesen/Schreiben<br/> | Legt den aktuellen Wert einer Eigenschaft fest oder ruft ihn ab.<br/> |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |
| IID<br/>                      | CLSID \_ webwizardhost<br/>                                                        |



 

 




