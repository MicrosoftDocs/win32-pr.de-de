---
description: Die ikeyframecontrol-Schnittstelle wird von h. 323 MSP implementiert und ist nur für h. 323-Streamobjekte verfügbar.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Ikeyframecontrol-Schnittstelle (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368482"
---
# <a name="ikeyframecontrol-interface"></a>Ikeyframecontrol-Schnittstelle

\[**Ikeyframecontrol** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **ikeyframecontrol** -Schnittstelle wird von [h. 323 MSP](h323-msp.md) implementiert und ist nur für h. 323-Streamobjekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können. Sie verfügt über zwei Methoden, mit denen die Anwendung den Remote Endpunkt auffordern kann, das Video Bild mit einem Keyframe zu aktualisieren.

## <a name="members"></a>Member

Die **ikeyframecontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ikeyframecontrol** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ikeyframecontrol** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Periodicupdatepicture**](ikeyframecontrol-periodicupdatepicture.md) | Konfiguriert einen Timer im Stream, der regelmäßig Bildaktualisierungen anfordert.<br/> |
| [**Updatepicture**](ikeyframecontrol-updatepicture.md)                 | Fordert den Absender des Videos auf, das Bild zu aktualisieren.<br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[H323-msp](h323-msp.md)
</dt> </dl>

 

