---
description: Mit Windows 7 werden Bibliotheken eingeführt, die Benutzern eine einheitliche Ansicht Ihrer Dateien bereitstellen, auch wenn diese Dateien an unterschiedlichen Speicherorten gespeichert werden.
title: Windows-Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980936"
---
# <a name="windows-libraries"></a>Windows-Bibliotheken

Mit Windows 7 werden Bibliotheken eingeführt, die Benutzern eine einheitliche Ansicht Ihrer Dateien bereitstellen, auch wenn diese Dateien an unterschiedlichen Speicherorten gespeichert werden. Bibliotheken können von einem Benutzer konfiguriert und organisiert werden, und eine Bibliothek kann Ordner enthalten, die sich auf dem Computer des Benutzers und auch Ordner befinden, die über ein Netzwerk freigegeben wurden. Bibliotheken stellen eine einfachere Ansicht des zugrunde liegenden Speichersystems dar, denn für den Benutzer werden die Dateien und Ordner in einer Bibliothek in der einzelnen Ansicht angezeigt, unabhängig davon, wo Sie physisch gespeichert werden.

Entwickler, die neue Programme in Windows 7 schreiben, werden empfohlen, Bibliotheken als Mittel zu verwenden, mit denen die Benutzer mit den Dateien interagieren, die vom Programm verwendet werden. Die Verwendung von Bibliotheken in Ihrem Programm bietet Benutzern eine saubere, einfachere und einheitlichere Benutzerfreundlichkeit in Windows 7.

Entwickler sollten auch Ihre vorhandenen Programme überprüfen und ggf. aktualisieren, um mit Bibliotheken zu arbeiten. Da Bibliotheken nicht Teil des Dateisystems sind, haben Dateisystem basierte APIs keinen Zugriff auf Bibliotheken, die der Benutzer möglicherweise konfiguriert hat.

Programme, die derzeit zulassen, dass Benutzer ihre Inhalte in anderen Ordnern oder auf unterschiedlichen Computern speichern, werden am meisten davon profitieren, wenn Sie Bibliotheks Unterstützung hinzufügen. Bibliotheken vereinfachen die Verwaltung von Inhalten an verschiedenen Speicherorten für den Entwickler und den Benutzer.

In dieser Anleitung wird beschrieben, was Bibliotheken sind, wie Programme zum Arbeiten mit Bibliotheken erstellt werden können und wie ein Programmbibliotheken verwenden kann, um die Benutzeroberflächen zu verbessern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bibliotheken](library-leverage-to-manage-folders.md)
</dt> <dt>

[Verwenden von Bibliotheken in Ihrem Programm](library-be-library-aware.md)
</dt> <dt>

[**Ishelllibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shelllinks](./links.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> </dl>

 

 
