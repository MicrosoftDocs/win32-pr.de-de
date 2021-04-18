---
title: Iwmdrmlicenabmanagement-Schnittstelle
description: Die iwmdrmlicenabmanagement-Schnittstelle stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenz Speicher ausführen. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmlicenpasmanagement als riid-Parameter.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Iwmdrmlicenabmanagement Interface Windows Media-Format
- Iwmdrmlicensmanagement Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312480"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Iwmdrmlicenabmanagement-Schnittstelle

Die **iwmdrmlicenabmanagement** -Schnittstelle stellt Methoden bereit, die allgemeine Vorgänge im Zusammenhang mit dem lokalen Lizenz Speicher ausführen.

Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf. Übergeben Sie **IID \_ iwmdrmlicenpasmanagement** als *riid* -Parameter.

## <a name="members"></a>Member

Die **iwmdrmlicenermanagement** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md). **Iwmdrmlicensmanagement** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmlicenermanagement** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                               | BESCHREIBUNG                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Ruft asynchron eine Lizenz von einer angegebenen URL ab.<br/>                                                      |
| [**Backuplicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Erstellt eine Sicherung der Lizenzen im lokalen Lizenz Speicher.<br/>                                                 |
| [**Cleanlicenabstore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Entfernt markierte Lizenzen aus dem Lizenz Speicher und zerlegt den Speicher, um die Leistung zu verbessern.<br/>             |
| [**"-Enumeration"**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Erstellt ein Lizenz-Enumeratorobjekt, das anhand von Parameterwerten mit Lizenzinformationen aufgefüllt wird.<br/>            |
| [**"Featelicenserevocationchallenge"**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Generiert eine Lizenz Sperr Aufforderung.<br/>                                                                    |
| [**Delta eLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Löscht eine Lizenz aus dem temporären lokalen Lizenz Speicher.<br/>                                                    |
| [**Monitorlicensererwerbs**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.<br/>                                                      |
| [**Processlicenabdeletionmessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Löscht eine Lizenz, die für den ursprünglich mit einem anderen Inhalts Schutzsystem geschützten Inhalt importiert wurde.<br/> |
| [**Processlicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Widerruft Lizenzen aus dem lokalen Lizenz Speicher.<br/>                                                               |
| [**Restorelicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Stellt zuvor gesicherte Lizenzen wieder her.<br/>                                                                      |
| [**Storelicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Fügt eine Lizenz zum lokalen Lizenz Speicher hinzu.<br/>                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Iwmdrmeventgenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





