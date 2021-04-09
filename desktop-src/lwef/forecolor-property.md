---
title: ForeColor-Eigenschaft
description: ForeColor-Eigenschaft
ms.assetid: b5cef81b-55e1-49a5-bdbf-f7101520a13a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef05c9f51e040326c75f142e4649a8dbd0cfdbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855632"
---
# <a name="forecolor-property"></a>ForeColor-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt die Vordergrundfarbe zurück, die derzeit im Word-sprecherfenster für das angegebene Zeichen angezeigt wird.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent ***. Zeichen ("*** Merkmal-ID * * *"). Sprechblase. ForeColor**

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **ForeColor** -Eigenschaft gibt einen Wert zurück, der die Textfarbe in der Wort Sprechblase angibt. Der gültige Bereich für eine normale RGB-Farbe ist 0 bis 16.777.215 (&HFFFFFF). Das hohe Byte einer Zahl in diesem Bereich ist 0 (null). die unteren 3 Bytes, vom minimal bis zum höchst wertigen Byte, bestimmen die Größe von rot, grün und blau. Der rote, grüne und blaue Farbanteil werden jeweils durch eine Zahl zwischen 0 und 255 (&HFF) dargestellt.

 

 




