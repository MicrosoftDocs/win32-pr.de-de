---
title: Iwmdrmnetreceiver-Schnittstelle
description: Die iwmdrmnetreceiver-Schnittstelle stellt Methoden bereit, die für die Verwendung von Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger benötigt werden. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmnetreceiver als riid-Parameter.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format
- Iwmdrmnetreceiver-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389340"
---
# <a name="iwmdrmnetreceiver-interface"></a>Iwmdrmnetreceiver-Schnittstelle

Die **iwmdrmnetreceiver** -Schnittstelle stellt Methoden bereit, die für die Verwendung von Microsoft Windows Media DRM für Netzwerkgeräte als Empfänger benötigt werden.

Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf. Übergeben Sie **IID \_ iwmdrmnetreceiver** als *riid* -Parameter.

## <a name="members"></a>Member

Die **iwmdrmnetreceiver** -Schnittstelle erbt von [**iwmdrmeventgenerator**](iwmdrmeventgenerator.md). **Iwmdrmnetreceiver** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmnetreceiver** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                               | BESCHREIBUNG                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Getlicenanchallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Generiert eine Lizenz Aufforderung, die beim Anfordern geschützter Inhalte an den Sender gesendet wird.<br/>                     |
| [**Getregistrationchallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Generiert eine Registrierungs Aufforderung, die beim Registrieren oder erneuten Validieren des Empfängers an den Sender gesendet wird.<br/> |
| [**Processlicenseresponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Verarbeitet die vom Sender gesendete Lizenz Antwort als Antwort auf eine Lizenz Herausforderung.<br/>                              |
| [**Processregistrationresponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Verarbeitet die vom Sender gesendete Registrierungs Antwort als Antwort auf eine Registrierungs Aufforderung.<br/>                    |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Iwmdrmeventgenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Iwmdrmnettransmitter-Schnittstelle**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





