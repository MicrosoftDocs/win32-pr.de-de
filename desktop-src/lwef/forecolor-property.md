---
title: ForeColor-Eigenschaft
description: ForeColor-Eigenschaft
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebfc7f0b64a43f7ccb9075426a75df9a777fbb8b1e5e94cb16e747e0681cb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962760"
---
# <a name="forecolor-property"></a>ForeColor-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Vordergrundfarbe zurück, die derzeit im Wortsprechblasenfenster für das angegebene Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent***. Zeichen ("**_CharacterID_*_"). Balloon.ForeColor_*

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **ForeColor-Eigenschaft** gibt einen Wert zurück, der die Farbe des Texts in der Wortsprechblase angibt. Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF). Das hohe Byte einer Zahl in diesem Bereich ist gleich 0. die unteren 3 Bytes vom geringsten bis zum signifikantesten Byte bestimmen die Menge von Rot, Grün und Blau. Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.

 

 




