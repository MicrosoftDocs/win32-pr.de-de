---
title: BorderColor-Eigenschaft
description: BorderColor-Eigenschaft
ms.assetid: 7592db02-c157-45f4-bbcf-e6d5bd99e8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6812910c76ad46e7c065314d0b3e5f03d8a6ad6dcb7b918ef33b1a0315a0ad0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963330"
---
# <a name="bordercolor-property"></a>BorderColor-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Rahmenfarbe zurück, die derzeit für das WortSprechblasenfenster für das angegebene Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_")._ *Balloon.BorderColor

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF). Das hohe Byte einer Zahl in diesem Bereich ist gleich 0. die unteren 3 Bytes vom geringsten bis zum signifikantesten Byte bestimmen die Menge von Rot, Grün und Blau. Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.

 

 




