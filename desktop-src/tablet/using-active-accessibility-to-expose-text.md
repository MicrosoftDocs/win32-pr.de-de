---
description: Übersicht über die Verwendung von aktivem Barrierefreiheit zum verfügbar machen von Text.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Verwenden von Active Accessibility zur Offenlegung von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343668"
---
# <a name="using-active-accessibility-to-expose-text"></a>Verwenden von Active Accessibility zur Offenlegung von Text

Anwendungen können mit Microsoft Active Accessibility Text verfügbar machen. Die [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle, die in früheren Versionen von Active Accessibility definiert ist, ist jedoch nicht für das verfügbar machen großer Mengen an Rich-Text optimiert. Spätere Versionen definieren Schnittstellen, die für die Bereitstellung großer Mengen von Text-und Textattributen optimiert sind.

Um große Mengen an Text verfügbar zu machen, erstellen Sie separate Component Object Model (com)-Objekte, die [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)-und untergeordnete Elemente unterstützen, um die einzelnen Textelemente darzustellen. Ein Run ist eine Zeile oder ein Teil einer Zeile, die dieselbe Formatierung hat.

Active Accessibility macht nur den Text und seinen Speicherort verfügbar, verfügt aber über keinen Mechanismus, um die Formatierung des Texts verfügbar zu machen. Trotz dieser Einschränkungen verwenden einige Programme Active Accessibility, um Text verfügbar zu machen. Beispielsweise verwenden Microsoft Internet Explorer und Microsoft Visual Studio Active Accessibility, um große Mengen von Text verfügbar zu machen.

Weitere Informationen zum verfügbar machen von Text mithilfe Active Accessibility finden Sie unter [Barrierefreiheit](../accessibility/accessibility.md).

 

 
