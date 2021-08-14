---
description: In diesem Thema wird beschrieben, was Bibliotheken sind und wie sie Benutzern und Entwicklern von Vorteil sein können.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Informationen zu Bibliotheken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e63aef55513fb36f9a3cbfa71c1b7a79040fd7848468bd1216779cd034132d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049323"
---
# <a name="about-libraries"></a>Informationen zu Bibliotheken

In diesem Thema wird beschrieben, was Bibliotheken sind und wie sie Benutzern und Entwicklern von Vorteil sein können.

Bibliotheken sind benutzerdefinierte Sammlungen von Ordnern. Eine Bibliothek verfolgt den physischen Speicherort jedes Ordners, wodurch der Benutzer und die Software dieser Aufgabe entlastet werden. Benutzer können verwandte Ordner in einer Bibliothek gruppieren, auch wenn diese Ordner auf verschiedenen Festplatten oder computern gespeichert sind.

In einer Bibliothek werden die Ordner und Dateien dem Benutzer als einzelne Sammlung angezeigt, und mithilfe der Shellbibliotheks-API kann der Inhalt der Bibliothek auch an einem einzigen Speicherort eines Programms angezeigt werden.

In einer Bibliothek können die Inhalte, z. B. Dokumente, Fotos, Videos oder Musik eines Benutzers, sortiert und angezeigt werden, wie es der Benutzer möchte, und nicht einfach so, wie es das Dateisystem erfordert. Beispielsweise können Benutzer den Inhalt einer Bibliothek mithilfe der Eigenschaften der Elemente in der Bibliothek organisieren, sodass verknüpfte Elemente auch dann zusammen sortiert werden, wenn sie in verschiedenen Ordnern gespeichert sind.

![Screenshot der Benutzeroberfläche der Bibliotheken](images/libraries-whatare.png)

In diesem Thema:

-   [Bibliotheksvorteile](#library-benefits)
    -   [Vorteile für Benutzer](#user-benefits)
    -   [Vorteile für Entwickler](#developer-benefits)
-   [Verwalten von Ordnern in Bibliotheken](#managing-folders-in-libraries)
-   [Zugehörige Themen](#related-topics)

## <a name="library-benefits"></a>Bibliotheksvorteile

In diesem Abschnitt werden einige der Vorteile von Bibliotheken aus Sicht des Endbenutzers und der Perspektive des Programmentwicklers beschrieben.

### <a name="user-benefits"></a>Vorteile für Benutzer

Das Hinzufügen von Bibliotheksunterstützung zu Ihrem Programm bietet dem Benutzer die folgenden Vorteile:

-   **Bibliotheken bieten eine konsistente Benutzeroberfläche in Windows 7**

    Die allgemeinen Dateidialogfelder unterstützen Bibliotheken und bieten die gleiche Benutzeroberfläche wie der Windows Explorer in Windows 7. Die Unterstützung von Bibliotheken in Ihrem Programm hilft, eine nahtlose Interaktion für den Benutzer zu ermöglichen, wenn Sie Ihr Programm in Windows 7 verwenden.

-   **Benutzer entscheiden, wo Inhalte gespeichert werden**

    Bibliotheken ermöglichen es Benutzern, zu steuern, wo ihre Inhalte gespeichert werden. Gleichzeitig bieten Bibliotheken angemessene Standardwerte für Benutzer, die diese Detailebene auf ihrem Computer nicht verwalten möchten. Benutzer entscheiden, wie viel oder wie wenig sie steuern möchten, wo und wie ihre Inhalte gespeichert werden, und die Bibliothek funktioniert in beiden Richtungen einwandfrei.

### <a name="developer-benefits"></a>Vorteile für Entwickler

Sie können Bibliotheken in Ihrem Programm verwenden, um eine flexiblere und komfortablere Benutzeroberfläche zu bieten, ohne viel komplexen Programmcode hinzufügen zu müssen. Zu den Vorteilen des Hinzufügens von Bibliotheksunterstützung gehören:

-   **Bibliotheken unterstützen Bibliotheks- und Dateisystemzugriff.**

    Mithilfe [**der Shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)können Programme Bibliotheksunterstützung für den Benutzer bereitstellen und gleichzeitig die Komplexität des Datei- und Ordnerverwaltungscodes reduzieren. Wenn Ihr Programm bereits die Dateisystem-API verwendet, können Sie so viel von diesem vorhandenen Code beibehalten, wie Sie möchten, und dennoch Bibliotheksunterstützung für den Benutzer bereitstellen, indem Sie die erforderlichen Dateisysteminformationen von der **Shellbibliothek-API abrufen.**

-   **Einfachere Änderungsbenachrichtigung**

    Sowohl das Dateisystem als auch die Shell-API können Ihr Programm benachrichtigen, wenn sich der Inhalt eines überwachten Ordners oder einer Bibliothek ändert. Mithilfe der Shell-API können Sie jedoch alle Ordner in der Bibliothek mit einer einzigen Benachrichtigung überwachen, auch wenn der Ordner in der Bibliothek auf verschiedenen Laufwerken oder sogar auf unterschiedlichen Computern gespeichert werden kann.

-   **Bibliotheken verwenden Dateieigenschaften.**

    Programme können die Dateieigenschaften verwenden, um zu steuern, welche Dateien während des Öffnens angezeigt werden, und Vorgänge speichern, die die allgemeinen Dateidialogfelder verwenden. Programme können auch über die [**IPropertyStore-Schnittstellen**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Zugriff auf Dateieigenschaften haben. Die allgemeinen Dateidialogfelder können auch konfiguriert werden, damit Benutzer die Eigenschaften aktualisieren können, die ihrem Inhalt zugeordnet sind.

-   **Programme können dedizierte Bibliotheken erstellen.**

    Eine neue Bibliothek kann erstellt werden, wenn vorhandene Benutzerbibliotheken die Anforderungen des Programms nicht erfüllen, z. B. wenn ein Programm einen neuen Benutzerinhaltstyp erstellt. Die neue Bibliothek kann mit einem eindeutigen Symbol konfiguriert werden, das ihren Inhalt darstellt und die Identifizierung der Bibliothek im Windows erleichtert.

## <a name="managing-folders-in-libraries"></a>Verwalten von Ordnern in Bibliotheken

Benutzer können ihre Bibliotheken organisieren, indem sie Ordner in der Bibliothek hinzufügen, verschieben oder entfernen. Nicht alle Ordner unterstützen jedoch alle Funktionen, die eine Bibliothek bereitstellen kann. Viele Bibliotheksfeatures erfordern schnellen Zugriff auf die verschiedenen Eigenschaften des Ordners und dessen Inhalte, die nur über die Windows sind. Um vollständige Bibliotheksfunktionen bereitstellen zu können, muss ein Ordner durch die Suche Windows werden können.

Eine Bibliothek lässt nicht zu, dass ein Benutzer Ordner hinzufüge, die keine vollständige Bibliotheksfunktionalität bieten. Die [**Shellbibliotheks-API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) kann jedoch solche Ordner hinzufügen. Wenn eine Bibliothek einen Ordner enthält, der keine vollständige Bibliotheksfunktionalität unterstützt, wird die Bibliothek in einem sicheren Modus ausgeführt und bietet eine eingeschränkte Funktionalität. In der folgenden Tabelle werden die Ordner beschrieben, die vollständige Bibliotheksfunktionen unterstützen, und ordner, die nicht unterstützt werden.



| Ordnertypen, die vollständige Bibliotheksfunktionen unterstützen                                                               | Ordnertypen, die keine vollständige Bibliotheksfunktionalität unterstützen                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Feste und externe NTFS- und FAT32-Festplatten.                                                                     | Wechseldatenträger, z. B. USB-Flashlaufwerke oder SD-Speicherkarten (Secure Digital).               |
| Dateifreigaben, die von der Windows Search indiziert werden, z. B. Abteilungsserver, Windows 7 oder Windows Vista-Heim-PCs. | Wechselmedien wie CD-ROM oder DVD-Medien.                                                 |
| Dateifreigaben, die offline verfügbar  sind, z. B. ein umgeleiteter Eigene Dokumente oder ein Client-Side Cache.        | Netzwerkfreigaben, die weder offline verfügbar noch remote indiziert sind, z. B. NAS-Laufwerke.   |
|                                                                                                                    | Andere Datenquellen wie Microsoft SharePoint, Microsoft Exchange und Microsoft OneDrive. |



 

Die folgende Abbildung zeigt die eingeschränkte Anzeige von Bibliotheksinhalten im abgesicherten Modus.

![Dialogfeld öffnen, wenn sich Bibliotheken im abgesicherten Modus befinden](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Bibliotheken](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Shelllinks](./links.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Schema der Bibliotheksbeschreibung](library-schema-entry.md)
</dt> </dl>

 

 
