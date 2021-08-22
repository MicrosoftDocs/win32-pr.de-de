---
title: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() über Windows Store-Apps wird nicht unterstützt.
description: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() über Windows Store-Apps wird nicht unterstützt.
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9950bc008ce96d6c0a80a6090c3312057a12c4a7a1f64a5563625a518831c27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119348570"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() über Windows Store-Apps wird nicht unterstützt.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>Beschreibung

Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() über eine Windows Store-App wird nicht unterstützt und kann zu unerwarteten Ergebnissen führen.

## <a name="manifestations"></a>Manifestationen

Beim Starten der Anwendung ist der IME-Modus auf die folgenden Standardwerte festgelegt:



| &nbsp;   | Softwareeingabebereich | Hardwaretastatur |
|----------|----------------------|-------------------|
| KOR, JPN | Ein                   | Aus               |
| CHS, CHT | Ein                   | Ein                |



 

## <a name="solution"></a>Lösung

Entwickler können den IME-Standardmodus steuern, indem sie einen Eingabebereichswert für das Feld angeben.

Der IME-Modus für einen angegebenen Eingabebereich wird von jedem IME bestimmt. Entwickler können den IME-Modus nicht angeben.

## <a name="resources"></a>Ressourcen

-   [InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 