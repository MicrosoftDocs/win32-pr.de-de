---
title: Codepages und Unicode-Zeichen folgen
description: Ein weiterer Aspekt bei der Implementierung von IPropertySetStorage ist, wie Unicode-Eigenschaftsnamen in der Eigenschaften-ID 0 (dem Eigenschaften Namen Wörterbuch) gespeichert werden, das keine Unicode-Zeichen folgen verwendet.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Codepages und Unicode-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309400"
---
# <a name="code-pages-and-unicode-strings"></a>Codepages und Unicode-Zeichen folgen

Ein weiterer Aspekt bei der Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ist, wie Unicode-Eigenschaftsnamen in der Eigenschaften-ID 0 (dem Eigenschaften Namen Wörterbuch) gespeichert werden, das keine Unicode-Zeichen folgen verwendet.

Unicode hat offiziell den Codepage-Wert 1200. Verwenden Sie zum Speichern von Unicode-Werten im Eigenschaften Namen Wörterbuch den Codepage-Wert 1200 für den gesamten Eigenschaften Satz (in der Eigen schafts-ID 1), der durch das Fehlen des **\_ ANSI-Flags propsetflag** in [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)angegeben wird. Beachten Sie, dass dies den Nebeneffekt hat, dass alle Zeichen folgen Werte in der in Unicode festgelegten Eigenschaft gespeichert werden. Bei allen Codepages ist die am Anfang eines **VT \_ LPSTR** gefundene Anzahl eine Byte Anzahl und keine Zeichen Anzahl. Dies ist erforderlich, um die Kompatibilität mit früheren Versionen zu gewährleisten.

Die Implementierung der Verbund Datei von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) erstellt alle neuen Eigenschaften Sätze vollständig entweder in Unicode (Codepage 1200) oder auf der aktuellen System-ANSI-Codepage. Dies wird dadurch gesteuert, dass das **propsetflag- \_ ANSI** -Flag im *grfFlags* -Parameter von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)fehlt oder vorhanden ist.

Erstellen und öffnen Sie Eigenschaften Sätze als Unicode. Um dies zu implementieren, legen Sie das **propsetflag- \_ ANSI** -Flag nicht im *grfFlags* -Parameter von [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)fest. Vermeiden Sie die Verwendung von **VT \_ LPSTR** -Werten, und verwenden Sie stattdessen **VT \_ LPWSTR** -Werte. Wenn die Codepage der Eigenschaft auf Unicode festgelegt ist, werden **VT \_ LPSTR** -Zeichen folgen Werte bei der Speicherung in Unicode konvertiert und beim Abrufen wieder in Multibytezeichen-Zeichen folgen Werte konvertiert.

Wenn Sie das **propsetflag- \_ ANSI** -Flag wie durch einen [**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) -aufrufen gemeldet festlegen, wird reflektiert, ob die zugrunde liegende Codepage oder nicht Unicode ist. Beachten Sie, dass die eigen schafts-ID 1 explizit gelesen werden kann, um die Codepage zu erlernen.

Sie können auf die Eigenschaften-ID 1 zugreifen, indem Sie [**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)aufrufen. Sie ist jedoch schreibgeschützt und kann nicht mit " [**Write-Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)" aktualisiert werden. Außerdem wird es möglicherweise nicht mit [**deletemultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)gelöscht.

 

 




