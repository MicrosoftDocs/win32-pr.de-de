---
title: Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt
description: Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101902"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Eingabemethoden-Manager-APIs werden vom vereinfachten Chinesisch (IME) nicht unterstützt

## <a name="platforms"></a>Plattformen

<dl> Clients-Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Die folgenden Eingabemethoden-Manager-APIs werden von vereinfachten chinesischen IMEs in Windows 8.1 nicht unterstützt:

-   Ifecommon-Schnittstelle
-   Ifedictionary-Schnittstelle
-   Ifelanguage-Schnittstelle
-   Iimepad-Schnittstelle
-   Iimepadapplet-Schnittstelle
-   Iimespecifyapplets-Schnittstelle

## <a name="manifestations"></a>Kundgebungen

Die Funktionen, die diese APIs verwenden, funktionieren nicht mit dem vereinfachten Chinesisch (IME).

## <a name="solution"></a>Lösung

Anwendungen müssen so entworfen werden, dass Benutzer die gewünschte Aufgabe ohne die angegebene API durchführen können.

## <a name="resources"></a>Ressourcen

-   [Schnittstellen für Eingabemethoden-Manager](../intl/input-method-manager-interfaces.md)
-   [Ifecommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Ifecommon-Schnittstelle](/windows/win32/api/msime/nn-msime-ifecommon)
-   [Ifedictionary-Schnittstelle](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [Ifelanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [Iimepad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [Iimepadapplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [Iimepluginditdiktattionarylist](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [Iimespecifyapplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 