---
title: WM/MCDI
description: Das WM/MCDI-Attribut enthält den Musik-CD-Bezeichner. Dabei handelt es sich um ein binäres Abbild des Inhaltsverzeichnisses von der CD, die zur eindeutigen Identifizierung der CD verwendet wird.
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- WM/MCDI Windows Media-Format
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106342100"
---
# <a name="wmmcdi"></a>WM/MCDI

Das **WM/MCDI-** Attribut enthält den Musik-CD-Bezeichner. Dabei handelt es sich um ein binäres Abbild des Inhaltsverzeichnisses von der CD, die zur eindeutigen Identifizierung der CD verwendet wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmmcdi

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ typbinär Datei**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist mit dem ID3-Frame (MCDI) kompatibel. Die ID3-Spezifikation für den MCDI-Frame erfordert, dass nur ein solcher Frame pro Datei vorhanden ist und dass ein gültiger trck-Frame vorhanden ist. Der Metadateneditor führt keine Validierung für diese Regeln aus. Außerdem ist die Größe von WM/MCDI nicht auf 804 bytes beschränkt, ebenso wie der MCDI ID3-Frame.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




