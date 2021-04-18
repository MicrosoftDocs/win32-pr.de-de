---
title: Remotedesktopdienste audioendpoint-Schnittstellen
description: Die folgenden Schnittstellen werden mit der audioendpoint-API verwendet.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337774"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Remotedesktopdienste audioendpoint-Schnittstellen

Die folgenden Schnittstellen werden mit der audioendpoint-API verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[**Iaudiodeviceendpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Initialisiert ein Geräte Endpunkt Objekt und ruft die Funktionen des Geräts ab, das es darstellt.

</dd> <dt>

[**Iaudioendpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Stellt Informationen für die Audioengine über einen audioendpunkt bereit. Diese Schnittstelle wird von einem audioendpunkt implementiert.

</dd> <dt>

[**Iaudioendpointcontrol**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Steuert den streamstatus eines Endpunkts.

</dd> <dt>

[**Iaudioendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Ruft den Unterschied zwischen den aktuellen Lese-und Schreib Positionen im Endpunkt Puffer ab.

</dd> <dt>

[**Iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Ruft den Eingabepuffer für jeden Verarbeitungs Durchlauf ab.

</dd> <dt>

[**Iaudiooutputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Ruft den Ausgabepuffer für jeden Verarbeitungs Durchlauf ab.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Remotedesktopdienste audioendpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. Es handelt sich nicht um Client Anwendungen.

 

 




