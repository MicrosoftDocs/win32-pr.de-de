---
title: Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen
description: Sie können die Benutzererfahrung mit Microsoft Windows Desktop Search (WDS) und Ihrem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9198fc56b8ca09e61909b1828d7d00b964bb12c0e13308583eb36a4e2211f3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976870"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Sie können die Benutzererfahrung mit Microsoft Windows Desktop Search (WDS) und Ihrem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren. Ohne weitere Erweiterung enthält der protokollhandler, den Sie erstellen, nicht die folgenden Benutzeroberflächen:

-   WDS zeigt keine bestimmten Symbole für Ihre Ergebnisse an.
-   Wenn Benutzer auf ein Element doppelklicken, reagiert die Benutzeroberfläche nicht auf das Ereignis.
-   Wenn Benutzer mit der rechten Maustaste auf ein Element klicken, unterstützt das Kontextmenü keine Vorgänge für das Element.

**IShellFolder** benötigt minimale Implementierungen von **IPersist** und **IPersistFolder,** und eine minimale Implementierung von **IShellFolder** ist für **IContextMenu** und **IExtractIcon** erforderlich, die beiden Schnittstellen, die eine nahtlose Benutzererfahrung bieten.

 

## <a name="ipersist"></a>Ipersist

Die **IPersist-Schnittstelle** definiert die einzelne **GetClassID-Methode,** die zur Bereitstellung der CLSID eines Objekts entwickelt wurde, das dauerhaft im System gespeichert werden kann.



| Methode       | BESCHREIBUNG                                 |
|--------------|---------------------------------------------|
| GetClassID() | Gibt die ClassID des Protokollhandlers zurück. |



 

> [!Note]
>
> Die gleiche CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder implementiert werden.**

 

 

## <a name="ipersistfolder"></a>IPersistFolder

Die **IPersistFolder-Schnittstelle** wird verwendet, um Shellordnerobjekte zu initialisieren. Bei der Implementierung dieser Schnittstelle, die von **IPersist abgeleitet** ist, wird dem Ordner mitgeteilt, wo er sich im Shellnamespace befindet.



| Methode       | BESCHREIBUNG                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize() | Weist ein Shellordnerobjekt an, sich basierend auf den übergebenen Informationen selbst zu initialisieren, und gibt S \_ OK zurück. |



 

> [!Note]
>
> Die gleiche CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder implementiert werden.**

 

Sie verwenden diese Schnittstelle nicht direkt. Sie wird von der Dateisystemimplementierung der IShellFolder::BindToObject-Schnittstelle verwendet, wenn ein Shellordnerobjekt initialisiert wird.

 

## <a name="ishellfolder"></a>IShellFolder

Die **IShellFolder-Schnittstelle** wird zum Verwalten von Ordnern verwendet, und eine partielle Implementierung ist erforderlich, damit sich die für einen Protokollhandler implementierten Symbol- und Kontextschnittstellen auf der Benutzeroberfläche der Ergebnisse der Windows-Desktopsuche ordnungsgemäß verhalten. Der Großteil der erforderlichen Funktionalität wird über die **GetUIObjectOf-Methode** verfügbar gemacht. Mit dieser Methode kann ein Add-In die **Schnittstellen IExtractIcon** und **IContextMenu** abfragen.

Die **IShellFolder-Schnittstelle** verwendet PIDLs anstelle von URLs. Im Gegensatz zu den Anforderungen einer vollständigen Namespaceerweiterung können Add-Ins eine einfache IDL-Struktur verwenden, die nur die URL enthält.

Die folgenden Methoden von **IShellFolder** müssen implementiert werden. Beachten Sie, dass fünf dieser Methoden eine minimale Implementierung erfordern.



| Methode             | BESCHREIBUNG                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Gibt E \_ NOTIMPL zurück.                                                                                                                                                                                          |
| BindToStorage()    | Gibt E \_ NOTIMPL zurück.                                                                                                                                                                                          |
| CreateViewObject() | Gibt E \_ NOTIMPL zurück.                                                                                                                                                                                          |
| SetNameOf()        | Gibt E \_ NOTIMPL zurück.                                                                                                                                                                                          |
| ParseDisplayName() | Konvertiert eine URL in die PIDL-Struktur.                                                                                                                                                                        |
| CompareIDs()       | Vergleicht zwei PIDL-Werte                                                                                                                                                                                    |
| GetDisplayNameOf() | Gibt die URL für eine PIDL zurück.                                                                                                                                                                                  |
| GetUIObjectOf()    | Diese Methode ähnelt der OLE COM QueryInterface-Methode. Wenn ein Symbol angefordert wird, fordert der Aufrufer die IID IExtractIcon an. Wenn ein Kontextmenü angefordert wird, fordert der \_ Aufrufer das \_ IID-IContextMenu an. |



 

> [!Note]
>
> Die gleiche CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder implementiert werden.**

 

**IShellFolder** wird nicht zum Aufzählen von Ordnern verwendet. Dies bedeutet, dass der Anzeigename eines Ordners die physische URL ist. Dies kann sich in Zukunft ändern.

 

## <a name="icontextmenu"></a>IContextMenu

Wenn WDS dem Benutzer Ergebnisse anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü anzeigen, das von Ihrer **IContextMenu-Schnittstelle definiert** wird.

Die Standardaktion im Kontextmenü ist die gleiche Aktion, die beim Doppelklicken auf das Element ergriffen wird. Ohne die entsprechenden **IShellFolder-** oder **IContextMenu-Schnittstellen** für das Element besteht das Standardverhalten für ein Doppelklickereignis im Übergeben der URL als Argument an die ShellExecute-Funktion.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** ruft ein Symbol für die WDS-Benutzeroberfläche basierend auf der URL in der VON Ihrem Protokollhandler bereitgestellten PIDL ab.

 

## <a name="code-sample"></a>Codebeispiel

Der [Benutzerdefinierte Protokollhandler Benutzeroberfläche Beispielcode](-search-2x-wds-ph-ui-samplecode.md) veranschaulicht eine Implementierung von **IShellFolder** und unterstützende Schnittstellen und bietet Unterstützung für die Bearbeitung der PIDLs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Benutzerdefinierter Protokollhandler Benutzeroberfläche Beispielcode](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




