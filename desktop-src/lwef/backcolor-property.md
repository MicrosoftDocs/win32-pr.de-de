---
title: BackColor-Eigenschaft (Features der Legacy-Windows-Umgebung)
description: BackColor-Eigenschaft
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332fcc6a9081b52300dbee4c69c77602e84a62e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739656"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>BackColor-Eigenschaft (Features der Legacy-Windows-Umgebung)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Hintergrundfarbe zurück, die derzeit im Word-sprecherfenster für das angegebene Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("**_Merkmal-ID_*_"). Sprechblase. BackColor_*

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF). Das hohe Byte einer Zahl in diesem Bereich ist 0 (null). die unteren 3 Bytes, vom minimal bis zum höchst wertigen Byte, bestimmen die Größe von rot, grün und blau. Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.

 

 




