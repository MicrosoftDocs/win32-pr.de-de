---
description: Die IMulticastControl-Schnittstelle wird vom IPConf-MSP implementiert und ist nur für Multicastaufrufobjekte verfügbar.
ms.assetid: 9bdb4ab9-30b3-46fb-b13a-de9c294c8046
title: IMulticastControl-Schnittstelle (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7469ca26a49bc25b36ae87727a1fdcf324bcf54e8a253805ed56f252c7f062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905950"
---
# <a name="imulticastcontrol-interface"></a>IMulticastControl-Schnittstelle

\[**IMulticastControl** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die **IMulticastControl-Schnittstelle** wird vom IPConf-MSP implementiert und ist nur für Multicastaufrufobjekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die die Erstellung und Bearbeitung von Terminals ermöglichen, die zwischen H323- und SDP-Clients kommunizieren können. Die **IMulticastControl-Schnittstelle** steuert den Multicast-Loopbackmodus.

Im MM NO LOOPBACK-Modus ist \_ multicast loopback deaktiviert. Das bedeutet, dass zwei Anwendungen auf demselben Computer, die derselben Multicastgruppe beitreten, die Pakete der anderen \_ erhalten. Dieser Modus bietet die beste Leistung, wenn immer nur eine Anwendung der Multicastgruppe auf dem Computer beitritt. Der MM \_ NO \_ LOOPBACK-Modus ist der Standardmodus.

Der MM \_ FULL \_ LOOPBACK-Modus ist nur zum Testen geeignet. Alle gesendeten Pakete werden auch in einer Schleife zurückverschleifet. Dies kann verwendet werden, um zu testen, ob die Geräte funktionieren.

Der MM SELECTIVE LOOPBACK-Modus wird verwendet, um mehreren Anwendungen auf einem Computer das Beitreten \_ \_ zur gleichen Multicastgruppe zu ermöglichen. Die Pakete werden vom Stapel zurückverschleifet, und jede RTP-Sitzung ist für das Herausfiltern unerwünschter Pakete verantwortlich.

## <a name="members"></a>Member

Die **IMulticastControl-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMulticastControl** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMulticastControl-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                  |
|:----------------------------------------------------------------|:---------------------------------------------|
| [**get \_ LoopbackMode**](imulticastcontrol-get-loopbackmode.md) | Ruft den Multicast-Loopbackmodus ab.<br/> |
| [**put \_ LoopbackMode**](imulticastcontrol-put-loopbackmode.md) | Legt den Multicast-Loopbackmodus fest.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Bibliothek<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> </dl>

 

