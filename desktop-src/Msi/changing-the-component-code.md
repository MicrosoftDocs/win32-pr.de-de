---
description: Beim Angeben der Komponenten für eine Installation sollten Paketautoren die allgemeinen Regeln für die Komponentenorganisation befolgen, die unter Organisieren von Anwendungen in Komponenten beschrieben werden.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Ändern des Komponentencodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96217dbcdbdc63d444f95d73dec657cf1a5ddef4ed80128c85b7752e1ec0f0d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520200"
---
# <a name="changing-the-component-code"></a>Ändern des Komponentencodes

Beim Angeben der [Komponenten](windows-installer-components.md) für eine Installation sollten Paketautoren die allgemeinen Regeln für die Komponentenorganisation befolgen, die unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)beschrieben werden. Autoren müssen möglicherweise neue Komponenten einführen oder vorhandene Komponenten ändern. Wenn durch das Hinzufügen, Entfernen oder Ändern von Ressourcen effektiv eine neue Komponente erstellt wird, muss auch der Komponentencode geändert werden.

## <a name="creating-a-new-component"></a>Erstellen einer neuen Komponente

Führen Sie eine neue Komponente ein, und weisen Sie ihr einen eindeutigen Komponentencode zu, wenn Sie eine der folgenden Änderungen vornehmen:

-   Jede Änderung, die beim Testen nicht angezeigt wurde, um mit früheren Versionen der Komponente kompatibel zu sein. In diesem Fall müssen Sie auch den Namen oder den Zielspeicherort jeder Ressource in der Komponente ändern.
-   Eine Änderung des Namens oder Zielspeicherorts einer beliebigen Datei, eines Registrierungsschlüssels, einer Verknüpfung oder einer anderen Ressource in der Komponente. In diesem Fall müssen Sie auch den Namen oder den Zielspeicherort jeder Ressource in der Komponente ändern.
-   Das Hinzufügen oder Entfernen einer Beliebigen Datei, eines Registrierungsschlüssels, einer Verknüpfung oder einer anderen Ressource aus der Komponente. In diesem Fall müssen Sie auch den Namen oder den Zielspeicherort jeder Ressource in der Komponente ändern.
-   Erneutes Kompilieren einer 32-Bit-Komponente in eine 64-Bit-Komponente.

Bei der Einführung einer neuen Komponente müssen Autoren eine der folgenden Schritte ausführen, um sicherzustellen, dass die Komponente nicht mit vorhandenen Komponenten in Konflikt steht:

-   Ändern Sie den Namen oder den Zielspeicherort einer Ressource, die von einer anderen Komponente unter dem gleichen Namen und Zielspeicherort installiert werden kann.
-   Andernfalls wird sichergestellt, dass die neue Komponente nie im selben Ordner wie eine andere Komponente installiert wird, die eine Ressource unter einem gemeinsamen Namen und Speicherort enthält. Dies schließt lokalisierte Versionen von Dateien mit dem gleichen Dateinamen ein. Weitere Informationen finden Sie unter [Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md).
-   Wenn Sie den Komponentencode einer vorhandenen Komponente ändern, ändern Sie auch den Namen oder den Zielspeicherort jeder Datei, jedes Registrierungsschlüssels, jeder Verknüpfung und jeder anderen Ressource in der Komponente.

### <a name="creating-a-new-version-of-a-component"></a>Erstellen einer neuen Version einer Komponente

Einer neuen Version einer Komponente wird der gleiche Komponentencode wie einer anderen vorhandenen Komponente zugewiesen. Das Ändern einer Komponente ohne Änderung des Komponentencodes ist nur in den folgenden Fällen optional:

-   Die Änderungen an der Komponente wurden durch Tests als abwärtskompatibel mit allen vorherigen Versionen der Komponente bestätigt.
-   Der Autor kann garantieren, dass die neue Version der Komponente nie auf einem System installiert wird, auf dem sie mit früheren Versionen der Komponente oder Anwendungen in Konflikt stehen würde, die eine frühere Version erfordern. Weitere Informationen finden Sie unter [Was geschieht, wenn die Komponentenregeln verletzt werden?](what-happens-if-the-component-rules-are-broken.md).

Der Komponentencode einer neuen Version einer Komponente darf nicht geändert werden, wenn dies dazu führen würde, dass zwei Komponenten Ressourcen gemeinsam nutzen, z. B. Registrierungswerte, Dateien oder Verknüpfungen.

 

 



