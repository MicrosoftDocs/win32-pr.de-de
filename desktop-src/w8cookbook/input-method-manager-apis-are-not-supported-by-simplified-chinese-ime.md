---
title: Eingabemethoden-Manager-APIs werden vom vereinfachten chinesischen IME nicht unterstützt.
description: Eingabemethoden-Manager-APIs werden vom vereinfachten chinesischen IME nicht unterstützt.
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0454df8df722992e321fd7fc6bd745382ea215116b2fd5a7797f2032a9c7e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935410"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a>Eingabemethoden-Manager-APIs werden vom vereinfachten chinesischen IME nicht unterstützt.

## <a name="platforms"></a>Plattformen

<dl> Clients – Windows 8.1  
Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

Die folgenden Eingabemethoden-Manager-APIs werden von vereinfachten chinesischen IMEs in Windows 8.1 nicht unterstützt:

-   IFECommon-Schnittstelle
-   IFEDictionary-Schnittstelle
-   IFELanguage-Schnittstelle
-   IImePad-Schnittstelle
-   IImePadApplet-Schnittstelle
-   IImeSpecifyApplets-Schnittstelle

## <a name="manifestations"></a>Manifestationen

Die Funktionen, die diese APIs verwenden, funktionieren nicht mit vereinfachtem chinesischem IME.

## <a name="solution"></a>Lösung

Anwendungen müssen so entworfen werden, dass Benutzer die gewünschte Aufgabe ausführen können, ohne die angegebene API zu verwenden.

## <a name="resources"></a>Ressourcen

-   [Schnittstellen des Eingabemethoden-Managers](../intl/input-method-manager-interfaces.md)
-   [IFECommon](/windows/win32/api/msime/nn-msime-ifecommon)
-   [IFECommon-Schnittstelle](/windows/win32/api/msime/nn-msime-ifecommon)
-   [IFEDictionary-Schnittstelle](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [IFELanguage](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [IImePad](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [IImePadApplet](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [IimePlugInDictDictionaryList](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [IImeSpecifyApplets](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 