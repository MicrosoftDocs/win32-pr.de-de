---
description: In diesem Thema wird beschrieben, was Bibliotheken sind und wie Sie von Benutzern und Entwicklern profitieren können.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Informationen zu Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557755"
---
# <a name="about-libraries"></a>Informationen zu Bibliotheken

In diesem Thema wird beschrieben, was Bibliotheken sind und wie Sie von Benutzern und Entwicklern profitieren können.

Bibliotheken sind benutzerdefinierte Auflistungen von Ordnern. In einer Bibliothek wird der physische Speicherort jedes Ordners nachverfolgt, wodurch der Benutzer und die Software dieser Aufgabe entlastet werden. Benutzer können verwandte Ordner in einer Bibliothek gruppieren, auch wenn diese Ordner auf unterschiedlichen Festplatten oder auf unterschiedlichen Computern gespeichert sind.

In einer Bibliothek werden die Ordner und Dateien für den Benutzer als einzelne Sammlung angezeigt. mithilfe der shellbibliotheks-API kann der Inhalt der Bibliothek auch an einem einzigen Speicherort zu einem Programm stehen.

In einer Bibliothek können die Inhalte, wie z. b. Dokumente, Fotos, Videos oder Musik eines Benutzers, sortiert und angezeigt werden, wenn der Benutzer das gewünschte Dateisystem benötigt. Beispielsweise können Benutzer den Inhalt einer Bibliothek mithilfe der Eigenschaften der Elemente in der Bibliothek organisieren, sodass Verwandte Elemente auch dann zusammen sortiert werden, wenn Sie in unterschiedlichen Ordnern gespeichert sind.

![Screenshot der Benutzeroberfläche "Bibliotheken"](images/libraries-whatare.png)

In diesem Thema:

-   [Bibliotheks Vorteile](#library-benefits)
    -   [Benutzer Vorteile](#user-benefits)
    -   [Vorteile für Entwickler](#developer-benefits)
-   [Verwalten von Ordnern in Bibliotheken](#managing-folders-in-libraries)
-   [Zugehörige Themen](#related-topics)

## <a name="library-benefits"></a>Bibliotheks Vorteile

In diesem Abschnitt werden einige der Vorteile von Bibliotheken aus der Perspektive des Endbenutzers und der Perspektive des Programm Entwicklers beschrieben.

### <a name="user-benefits"></a>Benutzer Vorteile

Das Hinzufügen von Bibliotheks Unterstützung zu Ihrem Programm bietet dem Benutzer die folgenden Vorteile:

-   **Bibliotheken stellen eine konsistente Benutzeroberfläche in Windows 7 bereit.**

    Die Dialogfelder allgemeine Dateien unterstützen Bibliotheken und bieten dieselbe Benutzer Darstellung wie Windows-Explorer in Windows 7. Unterstützende Bibliotheken in Ihrem Programm helfen bei der Verwendung des Programms in Windows 7 dabei, eine nahtlose Interaktion für den Benutzer bereitzustellen.

-   **Benutzer entscheiden, wo Inhalte gespeichert werden sollen.**

    Bibliotheken ermöglichen es Benutzern, den Speicherort Ihrer Inhalte zu steuern. Gleichzeitig bieten Bibliotheken angemessene Standardeinstellungen für Benutzer, die diese Detailebene nicht auf Ihrem Computer verwalten möchten. Benutzer entscheiden, wie viel oder wie wenig Sie steuern möchten, wo und wie Ihre Inhalte gespeichert werden und wie die Bibliothek in jedem Fall ordnungsgemäß funktioniert.

### <a name="developer-benefits"></a>Vorteile für Entwickler

Sie können Bibliotheken in Ihrem Programm verwenden, um eine flexiblere und bequeme Benutzeroberfläche bereitzustellen, ohne viel komplexen Programmcode hinzufügen zu müssen. Zu den Vorteilen beim Hinzufügen von Bibliotheks Unterstützung gehören:

-   **Bibliotheken unterstützen Bibliothek-und Dateisystem Zugriff**

    Mithilfe der [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)können Programme für den Benutzer Bibliotheks Unterstützung bereitstellen und gleichzeitig die Komplexität des Datei-und Ordner Verwaltungs Codes verringern. Wenn das Programm die Dateisystem-API bereits verwendet, können Sie den vorhandenen Code beliebig beibehalten und dem Benutzer dennoch Bibliotheks Unterstützung bereitstellen, indem Sie die erforderlichen Dateisystem Informationen aus der **shellbibliotheks-API** erhalten.

-   **Einfachere Änderungs Benachrichtigung**

    Sowohl das Dateisystem als auch die Shell-API können das Programm Benachrichtigen, wenn sich der Inhalt eines überwachten Ordners oder einer Bibliothek ändert. Mithilfe der Shell-API können Sie jedoch alle Ordner in der Bibliothek mit einer einzelnen Benachrichtigung überwachen, auch wenn der Ordner in der Bibliothek möglicherweise auf unterschiedlichen Laufwerken oder sogar auf unterschiedlichen Computern gespeichert ist.

-   **Bibliotheken verwenden von Dateieigenschaften**

    Programme können die Dateieigenschaften verwenden, um zu steuern, welche Dateien während der Öffnungs-und Speichervorgänge angezeigt werden, die die allgemeinen Datei Dialogfelder verwenden. Programme können auch über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstellen auf Dateieigenschaften zugreifen. Die Dialogfelder für die gemeinsame Datei können auch so konfiguriert werden, dass Benutzer die dem Inhalt zugeordneten Eigenschaften aktualisieren können.

-   **Programme können dedizierte Bibliotheken erstellen**

    Eine neue Bibliothek kann erstellt werden, wenn vorhandene Benutzer Bibliotheken die Programmanforderungen nicht erfüllen – beispielsweise, wenn ein Programm einen neuen Typ von Benutzer Inhalt erstellt. Die neue Bibliothek kann mit einem eindeutigen Symbol konfiguriert werden, das ihren Inhalt darstellt und die Identifizierung der Bibliothek im Windows-Explorer erleichtert.

## <a name="managing-folders-in-libraries"></a>Verwalten von Ordnern in Bibliotheken

Benutzer können Ihre Bibliotheken organisieren, indem Sie Ordner in der Bibliothek hinzufügen, verschieben oder entfernen. Nicht alle Ordner unterstützen jedoch die gesamte Funktionalität, die eine Bibliothek bereitstellen kann. Viele Bibliotheks Features erfordern einen schnellen Zugriff auf die verschiedenen Eigenschaften des Ordners und dessen Inhalte, die nur über Windows Search verfügbar sind. Um vollständige Bibliotheksfunktionen bereitzustellen, muss ein Ordner von Windows Search indiziert werden können.

In einer Bibliothek kann ein Benutzer keine Ordner hinzufügen, die keine vollständige Bibliotheks Funktionalität bereitstellen. Die [**shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) kann jedoch solche Ordner hinzufügen. Wenn eine Bibliothek einen Ordner enthält, der die Funktionalität der vollständigen Bibliothek nicht unterstützt, wird die Bibliothek in einem abgesicherten Modus betrieben und bietet eine eingeschränkte Funktionalität. In der folgenden Tabelle werden die Ordner beschrieben, die vollständige Bibliotheksfunktionen unterstützen.



| Ordner Typen, die vollständige Bibliotheksfunktionen unterstützen                                                               | Ordner Typen, die keine vollständige Bibliotheks Funktionalität unterstützen                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Feste und externe NTFS-und FAT32-Festplatten.                                                                     | Wechsel Datenträger, z. b. USB-Flash Laufwerke oder sichere digitale (SD) Speicherkarten.               |
| Dateifreigaben, die von Windows Search indiziert werden, z. b. Abteilungs Server, Windows 7 oder Windows Vista Home PCs. | Wechselmedien, z. b. CD-ROM oder DVD-Medien.                                                 |
| Offline verfügbare Dateifreigaben, z. b. ein umgeleiteter Ordner " **Eigene Dokumente** " oder ein Client-Side Cache.        | Netzwerkfreigaben, die weder Offline noch Remote indiziert sind, z. b. NAS-Laufwerke.   |
|                                                                                                                    | Andere Datenquellen, z. b. Microsoft SharePoint, Microsoft Exchange und Microsoft onedrive. |



 

In der folgenden Abbildung wird die eingeschränkte Anzeige der Bibliotheksinhalte im abgesicherten Modus gezeigt.

![Dialogfeld öffnen, wenn sich Bibliotheken im abgesicherten Modus befinden](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bibliotheken](library-leverage-to-manage-folders.md)
</dt> <dt>

[**Ishelllibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shelllinks](./links.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> </dl>

 

 
