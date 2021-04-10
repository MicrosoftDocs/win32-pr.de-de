---
description: Der sprach Datentyp ist eine Text Zeichenfolge, die mindestens eine gültige numerische Sprach-ID enthält. Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen diese durch Kommas getrennt werden.
ms.assetid: 547fc662-f055-421e-a621-eecdfa0b13f6
title: Sprache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc87cb8b88dc3a693eee6890276adb67ad359e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214630"
---
# <a name="language"></a>Sprache

Der sprach Datentyp ist eine Text Zeichenfolge, die mindestens eine gültige numerische Sprach-ID enthält. Wenn zwei oder mehr Sprach-IDs vorhanden sind, müssen diese durch Kommas getrennt werden.

Der sprach Datentyp ist ein 16-Bit-Wert, bei dem es sich um die Kombination aus einer primären und einer unter Sprachen numerischen ID handelt. Die primäre langid besteht aus den Bits 0 bis 9, während die unter Sprachen-ID Bits 10 bis 15 ist. Eine Liste der numerischen und numerischen IDs von Primär-und unter Sprachen finden Sie im Thema [sprach Bezeichner-Konstanten und-](../intl/language-identifier-constants-and-strings.md) Zeichen folgen.

Bei primären Sprach-IDs kann der Bereich von 0x200 bis 0x3ff vom Benutzer definiert werden. Der Bereich 0x000 bis 0x1FF ist für die Verwendung durch das System reserviert. Bei unter Sprachen-IDs ist der Bereich 0x20 bis 0x3f benutzerdefinierbar. Der Bereich 0x00 bis 0x1F ist für die Verwendung durch das System reserviert.

 

 
