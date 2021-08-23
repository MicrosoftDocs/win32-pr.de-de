---
description: In dieser Übersicht werden Fenstereigenschaften erläutert.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Informationen zu Fenstereigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c88657cba4cf12ed7ecedb07aeb545f8e4bf64109d34297637d734743d32dd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028498"
---
# <a name="about-window-properties"></a>Informationen zu Fenstereigenschaften

Bei *einer Fenstereigenschaft* handelt es sich um alle Daten, die einem Fenster zugewiesen sind. Eine Window-Eigenschaft ist normalerweise ein Handle der fensterspezifischen Daten, kann aber ein beliebiger Wert sein. Jede Fenstereigenschaft wird durch einen Zeichenfolgennamen identifiziert. Es gibt mehrere Funktionen, mit denen Anwendungen Fenstereigenschaften verwenden können. In dieser Übersicht werden die folgenden Themen erläutert:

-   [Vorteile der Verwendung von Fenstereigenschaften](#advantages-of-using-window-properties)
-   [Zuweisen von Fenstereigenschaften](#assigning-window-properties)
-   [Aufzählen von Fenstereigenschaften](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vorteile der Verwendung von Fenstereigenschaften

Fenstereigenschaften werden in der Regel verwendet, um Daten einem Unterklassenfenster oder einem Fenster in einer MDI-Anwendung (Multiple Document Interface) zu zuordnen. In beiden Fällen ist es aus zwei Gründen nicht praktisch, die zusätzlichen Bytes zu verwenden, die in der [**CreateWindow-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowa) oder -Klassenstruktur angegeben sind:

-   Eine Anwendung weiß möglicherweise nicht, wie viele zusätzliche Bytes verfügbar sind oder wie der Speicherplatz verwendet wird. Mithilfe von Fenstereigenschaften kann die Anwendung Daten einem Fenster zuordnen, ohne auf die zusätzlichen Bytes zugreifen zu müssen.
-   Eine Anwendung muss mithilfe von Offsets auf die zusätzlichen Bytes zugreifen. Auf Fenstereigenschaften wird jedoch über ihre Zeichenfolgenbezeichner zugegriffen, nicht über Offsets.

Weitere Informationen zum Unterklassening finden Sie unter [Window Procedure Subclassing](about-window-procedures.md). Weitere Informationen zu MDI-Fenstern finden Sie unter [Multiple Document Interface](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Zuweisen von Fenstereigenschaften

Die [**SetProp-Funktion**](/windows/win32/api/winuser/nf-winuser-setpropa) weist einem Fenster eine Fenstereigenschaft und ihren Zeichenfolgenbezeichner zu. Die [**GetProp-Funktion**](/windows/win32/api/winuser/nf-winuser-getpropa) ruft die Fenstereigenschaft ab, die durch die angegebene Zeichenfolge identifiziert wird. Die [**RemoveProp-Funktion**](/windows/win32/api/winuser/nf-winuser-removepropa) zerstört die Zuordnung zwischen einem Fenster und einer Fenstereigenschaft, aber nicht die Daten selbst. Um die Daten selbst zu zerstören, verwenden Sie die entsprechende Funktion, um das handle frei zu geben, das von **RemoveProp zurückgegeben wird.**

## <a name="enumerating-window-properties"></a>Aufzählen von Fenstereigenschaften

Die [**Funktionen EnumProps**](/windows/win32/api/winuser/nf-winuser-enumpropsa) und [**EnumPropsEx**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) aufzählen alle Eigenschaften eines Fensters mithilfe einer anwendungsdefinierten Rückruffunktion. Weitere Informationen zur Rückruffunktion finden Sie unter [*PropEnumProc*](/windows/win32/api/winuser/nc-winuser-propenumproca).

[**EnumPropsEx enthält**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) einen zusätzlichen Parameter für anwendungsdefinierte Daten, die von der Rückruffunktion verwendet werden. Weitere Informationen zur Rückruffunktion finden Sie unter [*PropEnumProcEx*](/windows/win32/api/winuser/nc-winuser-propenumprocexa).

 

 
