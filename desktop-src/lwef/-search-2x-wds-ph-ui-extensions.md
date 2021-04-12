---
title: Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen
description: Sie können die Benutzeroberflächen Funktionen von Microsoft Windows Desktop Search (WDS) und dem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2020
ms.locfileid: "104208747"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Hinzufügen von Symbolen und Kontextmenüs mit Shellerweiterungen

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Sie können die Benutzeroberflächen Funktionen von Microsoft Windows Desktop Search (WDS) und dem Protokollhandler verbessern, indem Sie Shellerweiterungen implementieren. Ohne weitere Erweiterung enthält der Protokollhandler, den Sie erstellen, nicht die folgenden Benutzeroberflächen:

-   In WDS werden keine spezifischen Symbole für Ihre Ergebnisse angezeigt.
-   Wenn Benutzer auf ein Element doppelklicken, reagiert die Benutzeroberfläche nicht auf das Ereignis.
-   Wenn Benutzer mit der rechten Maustaste auf ein Element klicken, werden keine Vorgänge für das Element vom Kontextmenü unterstützt.

Für **IShellFolder** sind minimale Implementierungen von **ipersistent** und **ipersistfolder** erforderlich, und für **IContextMenu** und **iextracticon** ist eine minimale Implementierung von **IShellFolder** erforderlich. die beiden Schnittstellen bieten eine nahtlose Benutzeroberfläche.

 

## <a name="ipersist"></a>IPersist

Die **ipersistent** -Schnittstelle definiert die einzelne **GetClassID-** Methode, die für die Bereitstellung der CLSID eines Objekts konzipiert ist, das im System dauerhaft gespeichert werden kann.



| Methode       | BESCHREIBUNG                                 |
|--------------|---------------------------------------------|
| GetClassID () | Gibt die ClassID des Protokoll Handlers zurück. |



 

> [!Note]
>
> Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.

 

 

## <a name="ipersistfolder"></a>Ipersistfolder

Die **ipersistfolder** -Schnittstelle wird verwendet, um Shellordner Objekte zu initialisieren. Die Implementierung dieser Schnittstelle, die von **ipersistent** abgeleitet wird, ist die Art und Weise, wie der Ordner im Shellnamespace informiert wird.



| Methode       | BESCHREIBUNG                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialisieren () | Weist ein shellordnerobjekt an, sich auf der Grundlage der bestandenen Informationen selbst zu initialisieren, und gibt S OK zurück. \_ |



 

> [!Note]
>
> Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.

 

Sie verwenden diese Schnittstelle nicht direkt. Sie wird von der Dateisystem Implementierung der IShellFolder:: bindtoken Object-Schnittstelle verwendet, wenn ein shellordnerobjekt initialisiert wird.

 

## <a name="ishellfolder"></a>IShellFolder

Die **IShellFolder** -Schnittstelle wird zum Verwalten von Ordnern verwendet, und eine partielle Implementierung ist erforderlich, damit die Symbol-und Kontext Schnittstellen, die für einen Protokollhandler implementiert werden, auf der Benutzeroberfläche der Windows-Desktop Suchergebnisse ordnungsgemäß Verhalten. Der größte Teil der erforderlichen Funktionalität wird durch die **getuiobjectof** -Methode verfügbar gemacht. Diese Methode ermöglicht es einem Add-in, die **iextracticon** -Schnittstelle und die **IContextMenu** -Schnittstelle abzufragen.

Die **IShellFolder** -Schnittstelle verwendet pidls anstelle von URLs. Im Gegensatz zu den Anforderungen einer kompletten Namespace Erweiterung können Add-Ins eine einfache IDL-Struktur verwenden, die nur die URL enthält.

Die folgenden Methoden von **IShellFolder** müssen implementiert werden. Beachten Sie, dass für fünf dieser Methoden eine minimale Implementierung erforderlich ist.



| Methode             | BESCHREIBUNG                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bindtoken ()     | Gibt E \_ notimpl zurück.                                                                                                                                                                                          |
| Bindesstorage ()    | Gibt E \_ notimpl zurück.                                                                                                                                                                                          |
| "Kreateviewobject ()" | Gibt E \_ notimpl zurück.                                                                                                                                                                                          |
| Setnameof ()        | Gibt E \_ notimpl zurück.                                                                                                                                                                                          |
| Parameydisplay Name () | Konvertiert eine URL in die PIDL-Struktur.                                                                                                                                                                        |
| Compareids ()       | Vergleicht zwei PIDL-Werte.                                                                                                                                                                                    |
| GetDisplayNameOf () | Gibt die URL für eine PIDL zurück.                                                                                                                                                                                  |
| Getuiobjectof ()    | Diese Methode ähnelt der OLE COM-QueryInterface-Methode. Wenn ein Symbol angefordert wird, fordert der Aufrufer die IID \_ iextracticon an. Wenn ein Kontextmenü angefordert wird, fordert der Aufrufer das IID \_ IContextMenu an. |



 

> [!Note]
>
> Die gleiche CLSID sollte für **ipersistent**, **ipersistfolder** und **IShellFolder** implementiert werden.

 

**IShellFolder** wird nicht zum Auflisten von Ordnern verwendet. Dies bedeutet, dass der Anzeige Name eines Ordners die physische URL ist. Dies kann sich in Zukunft ändern.

 

## <a name="icontextmenu"></a>IContextMenu

Wenn WDS Ergebnisse für den Benutzer anzeigt, kann der Benutzer mit der rechten Maustaste auf ein Element klicken und ein Kontextmenü sehen, das von der **IContextMenu** -Schnittstelle definiert wird.

Die Standardaktion im Kontextmenü ist dieselbe Aktion, die ausgeführt wird, wenn auf das Element Doppel geklickt wird. Ohne die entsprechenden **IShellFolder** -oder **IContextMenu** -Schnittstellen für das Element besteht das Standardverhalten eines Doppelklick Ereignisses darin, die URL als Argument an die ShellExecute-Funktion zu übergeben.

 

## <a name="iextracticon"></a>Iextracticon

**Iextracticon** Ruft ein Symbol für die WDS-Benutzeroberfläche basierend auf der URL in der PIDL ab, die von Ihrem Protokollhandler bereitgestellt wird.

 

## <a name="code-sample"></a>Codebeispiel

Der [Beispiel Code für die Benutzeroberfläche des benutzerdefinierten Protokoll Handlers](-search-2x-wds-ph-ui-samplecode.md) veranschaulicht eine Implementierung von **IShellFolder** und unterstützende Schnittstellen und bietet Unterstützung für die Bearbeitung der pidls.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Beispiel Code für die Benutzeroberfläche des benutzerdefinierten Protokoll Handlers](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




