---
description: In dieser Übersicht werden Fenster Eigenschaften erläutert.
ms.assetid: 67ca264e-af8e-41bf-b9d1-d3db8cf1cdc3
title: Informationen zu Fenster Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea646c594186b05bb74e70e6829f13a83cd0ec1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216081"
---
# <a name="about-window-properties"></a>Informationen zu Fenster Eigenschaften

Eine *Fenster Eigenschaft* sind alle Daten, die einem Fenster zugewiesen sind. Eine Fenster Eigenschaft ist in der Regel ein Handle der Fenster spezifischen Daten, kann jedoch ein beliebiger Wert sein. Jede Fenster Eigenschaft wird durch einen Zeichen folgen Namen identifiziert. Es gibt mehrere Funktionen, mit denen Anwendungen Fenster Eigenschaften verwenden können. In dieser Übersicht werden die folgenden Themen behandelt:

-   [Vorteile der Verwendung von Fenster Eigenschaften](#advantages-of-using-window-properties)
-   [Zuweisen von Fenster Eigenschaften](#assigning-window-properties)
-   [Auflisten von Fenster Eigenschaften](#enumerating-window-properties)

## <a name="advantages-of-using-window-properties"></a>Vorteile der Verwendung von Fenster Eigenschaften

Fenster Eigenschaften werden in der Regel verwendet, um Daten einem untergeordneten Fenster oder einem Fenster in einer MDI-Anwendung (Multiple Document Interface) zuzuordnen. In beiden Fällen ist es nicht sinnvoll, die zusätzlichen bytes, die in [**der Funktion oder der Klassen**](/windows/win32/api/winuser/nf-winuser-createwindowa) Struktur von "-Funktion" angegeben sind, aus den folgenden zwei Gründen zu verwenden:

-   Eine Anwendung weiß möglicherweise nicht, wie viele zusätzliche Bytes verfügbar sind oder wie der Speicherplatz verwendet wird. Mithilfe von Fenster Eigenschaften kann die Anwendung Daten einem Fenster zuordnen, ohne auf die zusätzlichen Bytes zuzugreifen.
-   Eine Anwendung muss mithilfe von Offsets auf die zusätzlichen Bytes zugreifen. Allerdings erfolgt der Zugriff auf Fenster Eigenschaften durch ihre Zeichen folgen Bezeichner, nicht durch Offsets.

Weitere Informationen zu Unterklassen finden Sie unter [Unterklassen für Fenster Prozeduren](about-window-procedures.md). Weitere Informationen zu MDI-Fenstern finden Sie unter [Multiple Document Interface](multiple-document-interface.md).

## <a name="assigning-window-properties"></a>Zuweisen von Fenster Eigenschaften

Die [**setprop**](/windows/win32/api/winuser/nf-winuser-setpropa) -Funktion weist einem Fenster eine Fenster Eigenschaft und deren Zeichen folgen Bezeichner zu. Die [**getprop**](/windows/win32/api/winuser/nf-winuser-getpropa) -Funktion Ruft die Fenster Eigenschaft ab, die durch die angegebene Zeichenfolge identifiziert wird. Die [**removeprop**](/windows/win32/api/winuser/nf-winuser-removepropa) -Funktion zerstört die Zuordnung zwischen einem Fenster und einer Fenster Eigenschaft, zerstört jedoch nicht die Daten selbst. Um die Daten selbst zu zerstören, verwenden Sie die entsprechende Funktion, um das von **removeprop** zurückgegebene Handle freizugeben.

## <a name="enumerating-window-properties"></a>Auflisten von Fenster Eigenschaften

Die Funktionen " [**EnumProperties**](/windows/win32/api/winuser/nf-winuser-enumpropsa) " und " [**enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) " zählen alle Eigenschaften eines Fensters mithilfe einer Anwendungs definierten Rückruffunktion auf. Weitere Informationen zur Rückruffunktion finden Sie unter " [*neigungsproc*](/windows/win32/api/winuser/nc-winuser-propenumproca)".

[**Enumpropsex**](/windows/win32/api/winuser/nf-winuser-enumpropsexa) enthält einen zusätzlichen Parameter für Anwendungs definierte Daten, die von der Rückruffunktion verwendet werden. Weitere Informationen zur Rückruffunktion finden Sie unter " [*neigungsprocex*](/windows/win32/api/winuser/nc-winuser-propenumprocexa)".

 

 
