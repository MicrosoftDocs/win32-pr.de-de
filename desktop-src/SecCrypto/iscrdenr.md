---
description: Stellt die Smartcard-Registrierungs Steuerung dar.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: Iscrdenr-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 3c3c882020db8b25c587a8d95824b3c90232bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361710"
---
# <a name="iscrdenr-interface"></a>Iscrdenr-Schnittstelle

Die **iscrdenr** -Schnittstelle stellt die Smartcard-Registrierungs Steuerung dar. Es ist hauptsächlich für Entwickler von Interesse, die Automatisierung nicht zu verwenden. Informationen zum Programmieren in Visual Basic oder einer anderen Automatisierungs Sprache finden Sie im [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) -Objekt.

## <a name="members"></a>Member

Die **iscrdenr** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Iscrdenr** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iscrdenr** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Fordert im Auftrag des Benutzers ein Zertifikat an und speichert das resultierende [*Zertifikat*](../secgloss/c-gly.md) auf der [*Smartcard*](../secgloss/s-gly.md)des Benutzers.<br/>                                                                                                                                                |
| [**enumcaname**](iscrdenr-enumcaname.md)                                 | Listet die Namen der [*Zertifizierungs*](../secgloss/c-gly.md) stellen (CAS) für einen angegebenen Namen für die Zertifikat Vorlage auf.<br/>                                                                                                                                                                                                       |
| [**enumcerttemplatename**](iscrdenr-enumcerttemplatename.md)             | Listet die Namen der Zertifikat Vorlagen auf.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumcspname**](iscrdenr-enumcspname.md)                               | Listet den Namen der verfügbaren [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) (CSPs) auf.<br/>                                                                                                                                                                                                               |
| [**getcacount**](iscrdenr-getcacount.md)                                 | Gibt die Anzahl der Zertifizierungsstellen zurück, die bereit sind, ein Zertifikat auf der Grundlage der angegebenen Zertifikat Vorlage auszustellen.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getcaname**](iscrdenr-getcaname.md)                                   | Ruft den Namen der angegebenen Zertifizierungsstelle für eine angegebene Zertifikat Vorlage ab.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getcerttemplatecount**](iscrdenr-getcerttemplatecount.md)             | Ruft die Anzahl der Zertifikat Vorlagen ab.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getcerttemplatename**](iscrdenr-getcerttemplatename.md)               | Ruft den Namen der Zertifikat Vorlage ab.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getcerttemplatesmime**](iscrdenr-getcerttemplatesmime.md)             | Stellen Sie fest, ob eine Zertifikat Vorlage die \_ \_ Verwendung des \_ e-Mail-Schutzes für den szoid-PKIX- \_ Schlüssel Wenn diese Schlüssel Verwendung Teil der Zertifikat Vorlage ist, werden von der Zertifikat Vorlage [*sichere/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) Vorgänge (S/MIME) unterstützt.<br/> |
| [**getenrolledcertifiupdatename**](iscrdenr-getenrolledcertificatename.md) | Ruft den Namen des Zertifikats ab, das sich aus einem früheren erfolgreichen Aufrufen von " [**iscrdenr:: Enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))" ergibt. Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen.<br/>                                                                                                                                                                                                 |
| [**getsigningcertifialisiename**](iscrdenr-getsigningcertificatename.md)   | Ruft den Antragsteller Namen aus dem Signaturzertifikat ab. Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Ruft den Namen des Benutzers ab, für den die Zertifikat Registrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetuser**](iscrdenr-resetuser.md)                                   | Löscht den Benutzernamen aus dem Smartcard-Steuerelement.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectsigningcertificate**](iscrdenr-selectsigningcertificate.md)     | Zeigt das Dialogfeld **Zertifikat auswählen** an, in dem ein Signaturzertifikat (auch als Registrierungs- *Agent-Zertifikat* bezeichnet) ausgewählt werden kann.<br/>                                                                                                                                                                                                                                                           |
| [**selectusername**](iscrdenr-selectusername.md)                         | Zeigt das Dialogfeld **Benutzer auswählen** an, in dem ein Benutzername ausgewählt werden kann. Der Benutzername gilt für den Benutzer, für den die Zertifikat Registrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                     |
| [**setcaname**](iscrdenr-setcaname.md)                                   | Gibt den Namen der Zertifizierungsstelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setcerttemplatename**](iscrdenr-setcerttemplatename.md)               | Gibt den Namen der Zertifikat Vorlage an.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Gibt ein Signaturzertifikat an (wird auch als Registrierungs- *Agent-Zertifikat* bezeichnet).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Gibt den Namen des Benutzers an, für den die Zertifikat Registrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **iscrdenr** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                         | Zugriffstyp           | BESCHREIBUNG                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**Cspcount**](iscrdenr-cspcount.md)<br/> | Schreibgeschützt<br/>  | Gibt die Anzahl der CSPs an. Diese Eigenschaft ist schreibgeschützt.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lesen/Schreiben<br/> | Der Name des CSP. Dies ist eine Eigenschaft mit Lese- und Schreibzugriff. <br/>        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



 

 
