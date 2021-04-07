---
title: Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.
description: Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727696"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus Windows Store-Apps wird nicht unterstützt.

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8,1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Das Aufrufen von immsetconfiguration Manager Status () oder immgetanversionstatus () aus einer Windows Store-App wird nicht unterstützt und kann zu unerwarteten Ergebnissen führen.

## <a name="manifestations"></a>Kundgebungen

Beim Starten der Anwendung wird der IME-Modus auf die folgenden Standardwerte festgelegt:



|          | Software Eingabebereich | Hardware Tastatur |
|----------|----------------------|-------------------|
| Kor, jpn | Ein                   | Aus               |
| CHS, cht | Ein                   | Ein                |



 

## <a name="solution"></a>Lösung

Entwickler können den Standard-IME-Modus steuern, indem Sie einen Eingabe Bereichs Wert für das Feld angeben.

Der IME-Modus für einen angegebenen Eingabebereich wird von jedem IME bestimmt. Entwickler können den IME-Modus nicht angeben.

## <a name="resources"></a>Ressourcen

-   [InputScope-Enumeration](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [Immsetsystemversionstatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [Immgetsystemversionstatus](/previous-versions/aa912903(v=msdn.10))

 

 