---
title: Iwmdrmnettransmitter-Schnittstelle
description: Die iwmdrmnettransmitter-Schnittstelle stellt Methoden bereit, die erforderlich sind, um Windows Media DRM für Netzwerkgeräte als Sender zu verwenden. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmnettransmitter als riid-Parameter.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315753"
---
# <a name="iwmdrmnettransmitter-interface"></a>Iwmdrmnettransmitter-Schnittstelle

Die **iwmdrmnettransmitter** -Schnittstelle stellt Methoden bereit, die erforderlich sind, um Windows Media DRM für Netzwerkgeräte als Sender zu verwenden.

Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf. Übergeben Sie **IID \_ iwmdrmnettransmitter** als *riid* -Parameter.

## <a name="members"></a>Member

Die **iwmdrmnettransmitter** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmnettransmitter** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmnettransmitter** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                        | BESCHREIBUNG                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Getleaflicenseresponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Generiert eine Blatt Lizenz-Antwortnachricht.<br/>                                                       |
| [**Getrootlicenseresponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Generiert eine Stamm Lizenz-Antwortnachricht.<br/>                                                        |
| [**Setlicensechallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Verarbeitet eine Lizenzanfrage, die von einem Microsoft Windows Media DRM für Netzwerkgeräte Empfänger gesendet wird.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> <dt>

[**Iwmdrmnetreceiver-Schnittstelle**](iwmdrmnetreceiver.md)
</dt> </dl>

 

