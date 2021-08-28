---
description: Stellt das Smartcard-Registrierungssteuerelement dar.
ms.assetid: ae872206-81e7-4627-b807-4222f75f8ab6
title: ISCrdEnr-Schnittstelle
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
ms.openlocfilehash: 2471f3acbb483af7e1882102527d392a69e2c7494a929f37718b51a17405c92b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867890"
---
# <a name="iscrdenr-interface"></a>ISCrdEnr-Schnittstelle

Die **ISCrdEnr-Schnittstelle** stellt das Smartcard-Registrierungssteuerelement dar. Es ist in erster Linie für Entwickler von Interesse, die Automation nicht verwenden. Informationen zum Programmieren in Visual Basic oder einer anderen Automation-Sprache finden Sie im [**CEnroll-Objekt.**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))

## <a name="members"></a>Member

Die **ISCrdEnr-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCrdEnr** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ISCrdEnr-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Registrieren**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))                                         | Fordert ein Zertifikat im Namen des Benutzers an und speichert das resultierende [*Zertifikat*](../secgloss/c-gly.md) auf der [*Smartcard*](../secgloss/s-gly.md)des Benutzers.<br/>                                                                                                                                                |
| [**enumCAName**](iscrdenr-enumcaname.md)                                 | Listet die Namen der [*Zertifizierungsstellen*](../secgloss/c-gly.md) für einen bestimmten Zertifikatvorlagennamen auf.<br/>                                                                                                                                                                                                       |
| [**enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)             | Listet die Namen der Zertifikatvorlagen auf.<br/>                                                                                                                                                                                                                                                                                                                                                               |
| [**enumCSPName**](iscrdenr-enumcspname.md)                               | Listet den Namen der verfügbaren [*Kryptografiedienstanbieter*](../secgloss/c-gly.md) auf.<br/>                                                                                                                                                                                                               |
| [**getCACount**](iscrdenr-getcacount.md)                                 | Gibt die Anzahl der Zertifizierungsstellen zurück, die bereit sind, ein Zertifikat basierend auf der angegebenen Zertifikatvorlage auszustellen.<br/>                                                                                                                                                                                                                                                                                                    |
| [**getCAName**](iscrdenr-getcaname.md)                                   | Ruft den Namen der angegebenen Zertifizierungsstelle für eine bestimmte Zertifikatvorlage ab.<br/>                                                                                                                                                                                                                                                                                                                                 |
| [**getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)             | Ruft die Anzahl der Zertifikatvorlagen ab.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**getCertTemplateName**](iscrdenr-getcerttemplatename.md)               | Ruft den Namen der Zertifikatvorlage ab.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**getCertTemplateSMIME**](iscrdenr-getcerttemplatesmime.md)             | Bestimmen Sie, ob eine Zertifikatvorlage die Verwendung des \_ SZOID PKIX \_ KP EMAIL \_ \_ PROTECTION-Schlüssels enthält. Wenn diese Schlüsselverwendung Teil der Zertifikatvorlage ist, unterstützt die Zertifikatvorlage [*S/MIME-Vorgänge (Secure/Multipurpose Internet Mail Extensions).*](../secgloss/s-gly.md)<br/> |
| [**getEnrolledCertificateName**](iscrdenr-getenrolledcertificatename.md) | Ruft den Namen des Zertifikats ab, der sich aus einem früheren erfolgreichen Aufruf von [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))ergibt. Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen.<br/>                                                                                                                                                                                                 |
| [**getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)   | Ruft den Antragstellernamen aus dem Signaturzertifikat ab. Diese Methode kann auch verwendet werden, um das Zertifikat in einem Dialogfeld anzuzeigen. <br/>                                                                                                                                                                                                                                                                       |
| [**getUserName**](iscrdenr-getusername.md)                               | Ruft den Namen des Benutzers ab, in dessen Namen die Zertifikatregistrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**resetUser**](iscrdenr-resetuser.md)                                   | Löscht den Benutzernamen aus dem Smartcard-Steuerelement.<br/>                                                                                                                                                                                                                                                                                                                                                        |
| [**selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)     | Zeigt ein Dialogfeld **Zertifikat auswählen** an, in dem ein Signaturzertifikat (auch als Zertifikat des *Registrierungs-Agents* bezeichnet) ausgewählt werden kann.<br/>                                                                                                                                                                                                                                                           |
| [**selectUserName**](iscrdenr-selectusername.md)                         | Zeigt ein Dialogfeld **Benutzer auswählen** an, in dem ein Benutzername ausgewählt werden kann. Der Benutzername gilt für den Benutzer, in dessen Namen die Zertifikatregistrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                     |
| [**setCAName**](iscrdenr-setcaname.md)                                   | Gibt den Namen der Zertifizierungsstelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**setCertTemplateName**](iscrdenr-setcerttemplatename.md)               | Gibt den Namen der Zertifikatvorlage an.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**setSigningCertificate**](iscrdenr-setsigningcertificate.md)           | Gibt ein Signaturzertifikat an (auch als *Registrierungs-Agent-Zertifikat* bezeichnet).<br/>                                                                                                                                                                                                                                                                                                                      |
| [**setUserName**](iscrdenr-setusername.md)                               | Gibt den Namen des Benutzers an, in dessen Namen die Zertifikatregistrierung vorgesehen ist.<br/>                                                                                                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **ISCrdEnr-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                         | Zugriffstyp           | BESCHREIBUNG                                                          |
|:-------------------------------------------------|:----------------------|:---------------------------------------------------------------------|
| [**CSPCount**](iscrdenr-cspcount.md)<br/> | Schreibgeschützt<br/>  | Gibt die Anzahl der CSPs an. Diese Eigenschaft ist schreibgeschützt.<br/> |
| [**CSPName**](iscrdenr-cspname.md)<br/>   | Lesen/Schreiben<br/> | Der Name des CSP. Dies ist eine Eigenschaft mit Lese- und Schreibzugriff. <br/>        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



 

 
