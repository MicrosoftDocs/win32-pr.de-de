---
title: Remotedesktopdienste AudioEndpoint-Schnittstellen
description: Die folgenden Schnittstellen werden mit der AudioEndpoint-API verwendet.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000070"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Remotedesktopdienste AudioEndpoint-Schnittstellen

Die folgenden Schnittstellen werden mit der AudioEndpoint-API verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Initialisiert ein Geräteendpunktobjekt und ruft die Funktionen des Geräts ab, das es darstellt.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Stellt der Audio-Engine Informationen zu einem Audioendpunkt bereit. Diese Schnittstelle wird von einem Audioendpunkt implementiert.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Steuert den Streamstatus eines Endpunkts.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Ruft den Unterschied zwischen der aktuellen Lese- und Schreibposition im Endpunktpuffer ab.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Ruft den Eingabepuffer für jeden Verarbeitungsdurchlauf ab.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Ruft den Ausgabepuffer für jeden Verarbeitungsdurchlauf ab.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Remotedesktopdienste AudioEndpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. sie ist nicht für Clientanwendungen vorgesehen.

 

 




