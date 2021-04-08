---
description: Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: DXVA-HD-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861803"
---
# <a name="dxva-hd-sample"></a>DXVA-HD-Beispiel

Zeigt, wie Microsoft DirectX Video Acceleration High Definition (DXVA-HD) verwendet wird.

Bei diesem Beispiel handelt es sich im Wesentlichen um einen Port des [DXVA2 \_ videoproc](dxva2-videoproc-sample.md)-Beispiels. Sie verfügt über die gleichen grundlegenden Funktionen, und die meisten Tastaturbefehle sind identisch.

Das Beispiel generiert Programm gesteuert Videos mit einem primären Stream und einem substream. Der primäre Stream zeigt SMPTE-Farb leisten an. Der unter Datenstrom wird mithilfe von Luma-Schlüssel auf dem primären Stream gemischt. Der Benutzer kann die Videoverarbeitungs Parameter ändern, einschließlich des planaren Alpha Werts, der Quell-und Ziel Rechtecke, Farbanpassungen und Farbraum. In der folgenden Abbildung wird das Video gezeigt, das generiert wird.

![Screenshot des Beispiels "DXVA-HD"](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden DXVA-HD-Schnittstellen veranschaulicht:

-   [**Idxvahd- \_ Gerät**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**Idxvahd \_ videoprocessor**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



