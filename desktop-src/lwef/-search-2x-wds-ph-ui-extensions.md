---
title: Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen
description: Sie können die Benutzerfreundlichkeit mit Microsoft Windows DesktopSuche (WDS) und Ihrem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren.
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
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search.](../search/-search-3x-wds-overview.md)

Sie können die Benutzerfreundlichkeit mit Microsoft Windows DesktopSuche (WDS) und Ihrem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren. Ohne weitere Erweiterung enthält der von Ihnen erstellte Protokollhandler nicht die folgenden Benutzeroberflächen:

-   WDS zeigt keine bestimmten Symbole für Ihre Ergebnisse an.
-   Wenn Benutzer auf ein Element doppelklicken, reagiert die Benutzeroberfläche nicht auf das Ereignis.
-   Wenn Benutzer mit der rechten Maustaste auf ein Element klicken, unterstützt das Kontextmenü keine Vorgänge für das Element.

Für **IShellFolder** sind minimale Implementierungen von **IPersist** und **IPersistFolder** erforderlich, und eine minimale Implementierung von **IShellFolder** ist für **IContextMenu** und **IExtractIcon** erforderlich, die zwei Schnittstellen, die eine nahtlosere Benutzeroberfläche bieten.

 

## <a name="ipersist"></a>Ipersist

Die **IPersist-Schnittstelle** definiert die einzelne **GetClassID-Methode,** die entwickelt wurde, um die CLSID eines Objekts zur Verfügung zu stellen, das dauerhaft im System gespeichert werden kann.



| Methode       | BESCHREIBUNG                                 |
|--------------|---------------------------------------------|
| GetClassID() | Gibt die ClassID des Protokollhandlers zurück. |



 

> [!Note]
>
> Dieselbe CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder** implementiert werden.

 

 

## <a name="ipersistfolder"></a>IPersistFolder

Die **IPersistFolder-Schnittstelle** wird verwendet, um Shellordnerobjekte zu initialisieren. Durch die Implementierung dieser Schnittstelle, die von **IPersist** abgeleitet wird, wird dem Ordner mitgeteilt, wo er sich im Shellnamespace befindet.



| Methode       | BESCHREIBUNG                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize() | Weist ein Shellordnerobjekt an, sich basierend auf den übergebenen Informationen selbst zu initialisieren, und gibt S OK zurück. \_ |



 

> [!Note]
>
> Dieselbe CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder** implementiert werden.

 

Sie verwenden diese Schnittstelle nicht direkt. Sie wird von der Dateisystemimplementierung der IShellFolder::BindToObject-Schnittstelle verwendet, wenn ein Shell-Ordnerobjekt initialisiert wird.

 

## <a name="ishellfolder"></a>IShellFolder

Die **IShellFolder-Schnittstelle** wird zum Verwalten von Ordnern verwendet, und es ist eine partielle Implementierung erforderlich, damit sich die für einen Protokollhandler implementierten Symbol- und Kontextschnittstellen auf der Benutzeroberfläche der Windows Desktopsuche-Ergebnisse ordnungsgemäß verhalten. Der Großteil der erforderlichen Funktionalität wird über die **GetUIObjectOf-Methode** verfügbar gemacht. Diese Methode ermöglicht ein Add-In zum Abfragen der **Schnittstellen IExtractIcon** und **IContextMenu.**

Die **IShellFolder-Schnittstelle** verwendet PIDLs anstelle von URLs. Im Gegensatz zu den Anforderungen einer vollständigen Namespaceerweiterung können Add-Ins eine einfache IDL-Struktur verwenden, die nur die URL enthält.

Die folgenden Methoden von **IShellFolder** müssen implementiert werden. Beachten Sie, dass fünf dieser Methoden eine minimale Implementierung erfordern.



| Methode             | BESCHREIBUNG                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Gibt E \_ NOTIMPL zurück                                                                                                                                                                                          |
| BindToStorage()    | Gibt E \_ NOTIMPL zurück                                                                                                                                                                                          |
| CreateViewObject() | Gibt E \_ NOTIMPL zurück                                                                                                                                                                                          |
| SetNameOf()        | Gibt E \_ NOTIMPL zurück                                                                                                                                                                                          |
| ParseDisplayName() | Konvertiert eine URL in die PIDL-Struktur.                                                                                                                                                                        |
| CompareIDs()       | Vergleicht zwei PIDL-Werte                                                                                                                                                                                    |
| GetDisplayNameOf() | Gibt die URL für eine PIDL zurück.                                                                                                                                                                                  |
| GetUIObjectOf()    | Diese Methode ähnelt der OLE COM QueryInterface-Methode. Wenn ein Symbol angefordert wird, fordert der Aufrufer das \_ IID-IExtractIcon an. Wenn ein Kontextmenü angefordert wird, fordert der Aufrufer den \_ IID-IContextMenu an. |



 

> [!Note]
>
> Dieselbe CLSID sollte für **IPersist,** **IPersistFolder** und **IShellFolder** implementiert werden.

 

**IShellFolder** wird nicht zum Aufzählen von Ordnern verwendet. Dies bedeutet, dass der Anzeigename eines Ordners die physische URL ist. Dies kann sich in Zukunft ändern.

 

## <a name="icontextmenu"></a>IContextMenu

Wenn WDS dem Benutzer Ergebnisse anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü anzeigen, das von ihrer **IContextMenu-Schnittstelle** definiert wird.

Die Standardaktion im Kontextmenü entspricht der Aktion, die beim Doppelklicken auf das Element ausgeführt wird. Ohne die entsprechenden **IShellFolder-** oder **IContextMenu-Schnittstellen** für das Element besteht das Standardverhalten für ein Doppelklickereignis darin, die URL als Argument an die ShellExecute-Funktion zu übergeben.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** ruft basierend auf der URL in der vom Protokollhandler bereitgestellten PIDL ein Symbol für die WDS-Benutzeroberfläche ab.

 

## <a name="code-sample"></a>Codebeispiel

Der [benutzerdefinierte Protokollhandler Benutzeroberfläche Beispielcode](-search-2x-wds-ph-ui-samplecode.md) veranschaulicht eine Implementierung von **IShellFolder** und unterstützende Schnittstellen und enthält Unterstützung für die Bearbeitung der PIDLs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Benutzerdefinierter Protokollhandler Benutzeroberfläche Beispielcode](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




