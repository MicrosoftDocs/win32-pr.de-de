---
description: Sie können die Funktionen "enumfonts" und "EnumFontFamilies" verwenden, um die Schriftarten aufzulisten, die in einem Drucker kompatiblen Speichergeräte Kontext verfügbar sind.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Überprüfen der Text Funktionen eines Geräts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994102"
---
# <a name="checking-the-text-capabilities-of-a-device"></a>Überprüfen der Text Funktionen eines Geräts

Sie können die Funktionen " [enumfonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) " und " [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) " verwenden, um die Schriftarten aufzulisten, die in einem Drucker kompatiblen Speichergeräte Kontext verfügbar sind. Sie können auch die [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) -Funktion verwenden, um Informationen über die Text Funktionen eines Geräts abzurufen. Indem Sie die [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) -Funktion mit dem numfonts-Index aufrufen, können Sie die minimale Anzahl von Schriftarten ermitteln, die von einem Drucker unterstützt werden. (Ein einzelner Drucker kann mehr Schriftarten unterstützen, als im Rückgabewert von **GetDeviceCaps** mit dem numfonts-Index angegeben.) Mit dem textcaps-Index können Sie viele der Text Funktionen des angegebenen Geräts identifizieren.

 

 
