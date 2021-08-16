---
description: Sie können die Funktionen EnumFonts und EnumFontFamilies verwenden, um die Schriftarten aufzuzählen, die in einem druckerkompatiblen Speichergerätekontext verfügbar sind.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Überprüfen der Textfunktionen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7121e7b5e2a416d06d79dba33c9a7c2eb7f6fb26d766a30b383f024e87e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119354850"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Überprüfen der Textfunktionen eines Geräts

Sie können die Funktionen [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) und [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) verwenden, um die Schriftarten aufzuzählen, die in einem druckerkompatiblen Speichergerätekontext verfügbar sind. Sie können auch die [GetDeviceCaps-Funktion](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) verwenden, um Informationen zu den Textfunktionen eines Geräts abzurufen. Durch Aufrufen der [**GetDeviceCaps-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) mit dem NUMFONTS-Index können Sie die Mindestanzahl von Schriftarten bestimmen, die von einem Drucker unterstützt werden. (Ein einzelner Drucker unterstützt möglicherweise mehr Schriftarten als im Rückgabewert von **GetDeviceCaps** mit dem NUMFONTS-Index angegeben.) Mithilfe des TEXTCAPS-Indexes können Sie viele der Textfunktionen des angegebenen Geräts identifizieren.

 

 
