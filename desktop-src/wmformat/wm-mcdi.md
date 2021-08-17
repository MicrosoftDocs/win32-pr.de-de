---
title: WM/MCDI
description: Das WM/MCDI-Attribut enthält den Musik-CD-Bezeichner. Dies ist ein binäres Speicherabbild des Inhaltsverzeichnis der CD, das zur eindeutigen Identifizierung der CD verwendet wird.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- WM/MCDI-Windows-Medienformat
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bccf4a081141c1902fe93680937a3196e015e6690acf76d69f3a3d8a016c092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963749"
---
# <a name="wmmcdi"></a>WM/MCDI

Das **WM/MCDI-Attribut** enthält den Musik-CD-Bezeichner. Dies ist ein binäres Speicherabbild des Inhaltsverzeichnis der CD, das zur eindeutigen Identifizierung der CD verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMMCDI

## <a name="data-type"></a>Datentyp

**\_WMT-TYP \_ BINARY**

## <a name="remarks"></a>Hinweise

Dieses Attribut ist mit dem ID3-Frame MCDI kompatibel. Die ID3-Spezifikation für den MCDI-Frame erfordert, dass nur ein solcher Frame pro Datei vorhanden ist und dass ein gültiger TRCK-Frame vorhanden ist. Der Metadaten-Editor führt keine Validierung für diese Regeln durch. Außerdem ist die Größe von WM/MCDI nicht auf 804 Byte beschränkt, ebenso wie der MCDI ID3-Frame.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




