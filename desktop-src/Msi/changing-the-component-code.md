---
description: Wenn Sie die Komponenten für eine-Installation angeben, sollten Paket Ersteller die allgemeinen Regeln für die Komponenten Organisation befolgen, die unter Organisieren von Anwendungen in Komponenten beschrieben werden.
ms.assetid: 7cf322e9-c49a-40a8-be4e-ab03ecba1c1f
title: Ändern des Komponenten Codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7531b4a38312d4abed038b612c4292c44af8e967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360484"
---
# <a name="changing-the-component-code"></a>Ändern des Komponenten Codes

Wenn Sie die [Komponenten](windows-installer-components.md) für eine-Installation angeben, sollten Paket Ersteller die allgemeinen Regeln für die Komponenten Organisation befolgen, die unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md)beschrieben werden. Autoren müssen möglicherweise neue Komponenten einführen oder vorhandene Komponenten ändern. Wenn durch das Hinzufügen, entfernen oder Ändern von Ressourcen eine neue Komponente erstellt wird, muss der Komponenten Code ebenfalls geändert werden.

## <a name="creating-a-new-component"></a>Erstellen einer neuen Komponente

Führen Sie eine neue-Komponente ein, und weisen Sie Ihr einen eindeutigen Komponenten Code zu, wenn Sie eine der folgenden Änderungen vornehmen:

-   Jede Änderung, die nicht durch Tests angezeigt wurde, um mit früheren Versionen der Komponente kompatibel zu sein. In diesem Fall müssen Sie auch den Namen oder den Ziel Speicherort jeder Ressource in der Komponente ändern.
-   Eine Änderung des Namens oder des Zielspeicher Orts von Dateien, Registrierungs Schlüsseln, Verknüpfungen oder anderen Ressourcen in der Komponente. In diesem Fall müssen Sie auch den Namen oder den Ziel Speicherort jeder Ressource in der Komponente ändern.
-   Das Hinzufügen oder Entfernen von Dateien, Registrierungs Schlüsseln, Verknüpfungen oder anderen Ressourcen aus der Komponente. In diesem Fall müssen Sie auch den Namen oder den Ziel Speicherort jeder Ressource in der Komponente ändern.
-   Erneutes Kompilieren einer 32-Bit-Komponente in eine 64-Bit-Komponente.

Beim Einführen einer neuen Komponente müssen Autoren eine der folgenden Aktionen durchführen, um sicherzustellen, dass die Komponente nicht mit vorhandenen Komponenten in Konflikt steht:

-   Ändern Sie den Namen oder den Zielort einer Ressource, die unter demselben Namen und Ziel Speicherort installiert werden kann, durch eine andere Komponente.
-   Stellen Sie andernfalls sicher, dass die neue Komponente niemals im selben Ordner wie eine andere Komponente installiert wird, die eine Ressource unter einem gemeinsamen Namen und Standort aufweist. Dies schließt lokalisierte Versionen von Dateien mit demselben Dateinamen ein. Weitere Informationen finden Sie unter [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md).
-   Wenn Sie den Komponenten Code einer vorhandenen Komponente ändern, ändern Sie auch den Namen oder den Ziel Speicherort für jede Datei, jeden Registrierungsschlüssel, jede Verknüpfung und jede andere Ressource in der Komponente.

### <a name="creating-a-new-version-of-a-component"></a>Erstellen einer neuen Version einer Komponente

Einer neuen Version einer Komponente wird derselbe Komponenten Code wie eine andere vorhandene Komponente zugewiesen. Das Ändern einer Komponente ohne Änderung des Komponenten Codes ist nur in den folgenden Fällen optional:

-   Die Änderungen an der Komponente wurden durch Tests überprüft, damit Sie abwärts kompatibel mit allen früheren Versionen der Komponente sind.
-   Der Autor kann sicherstellen, dass die neue Version der Komponente nie auf einem System installiert wird, auf dem Sie mit früheren Versionen der Komponente oder Anwendungen, die eine vorherige Version erfordern, in Konflikt steht. Weitere Informationen finden Sie unter [Was geschieht, wenn die Komponenten Regeln beschädigt sind?](what-happens-if-the-component-rules-are-broken.md).

Der Komponenten Code einer neuen Version einer Komponente darf nicht geändert werden, wenn dies dazu führen würde, dass zwei Komponenten Ressourcen gemeinsam nutzen, z. b. Registrierungs Werte, Dateien oder Verknüpfungen.

 

 



