---
title: BackColor-Eigenschaft (Legacy Windows Umgebungsfeatures)
description: BackColor-Eigenschaft
ms.assetid: a82c23bc-b280-4a52-9272-68879557cac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f799e8b9e00a97770cd004e29df75da8345a6cc01531fce53079ea550402c68d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114810"
---
# <a name="backcolor-property-legacy-windows-environment-features"></a>BackColor-Eigenschaft (Legacy Windows Umgebungsfeatures)

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Hintergrundfarbe zurück, die derzeit im Wortsprechblasenfenster für das angegebene Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Balloon.BackColor_*

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF). Das hohe Byte einer Zahl in diesem Bereich ist gleich 0. die unteren 3 Bytes vom geringsten bis zum signifikantesten Byte bestimmen die Menge von Rot, Grün und Blau. Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.

 

 




