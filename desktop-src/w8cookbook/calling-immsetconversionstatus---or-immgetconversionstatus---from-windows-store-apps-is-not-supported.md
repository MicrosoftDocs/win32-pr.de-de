---
title: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.
description: Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443145"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus Windows Store-Apps wird nicht unterstützt.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Server – Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Das Aufrufen von ImmSetConversionStatus() oder ImmGetConversionStatus() aus einer Windows Store-App wird nicht unterstützt und kann zu unerwarteten Ergebnissen führen.

## <a name="manifestations"></a>Manifestationen

Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:



| &nbsp;   | Softwareeingabebereich | Hardwaretastatur |
|----------|----------------------|-------------------|
| KOR, JPN | Ein                   | Aus               |
| CHS, CHT | Ein                   | Ein                |



 

## <a name="solution"></a>Lösung

Entwickler können den STANDARD-IME-Modus steuern, indem sie einen Eingabebereichswert für das Feld angeben.

Der IME-Modus für einen angegebenen Eingabebereich wird von jeder IME bestimmt. Entwickler können den IME-Modus nicht angeben.

## <a name="resources"></a>Ressourcen

-   [InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 