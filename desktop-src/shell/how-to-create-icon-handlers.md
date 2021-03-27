---
description: Beschreibt das Erstellen eines Handlers für benutzerdefinierte Symbol Zuweisungen.
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: Erstellen von Symbol Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979600"
---
# <a name="how-to-create-icon-handlers"></a>Erstellen von Symbol Handlern

Einem [Dateityp](fa-file-types.md) ist oft ein benutzerdefiniertes Symbol zugeordnet, damit seine Member in Windows-Explorer leicht erkennbar werden. Die einfachste Möglichkeit, einem Dateityp ein benutzerdefiniertes Symbol zuzuweisen, ist die Registrierung der Symbol Datei. Ein Symbol, das auf diese Weise registriert ist, ist jedoch für alle Member des Dateityps identisch. Sie können den Membern des Dateityps durch Implementieren eines *Symbol Handlers* viel mehr Flexibilität zuweisen.

Ein Symbol Handler ist ein Typ eines Shellerweiterungs Handlers, mit dem Sie den Membern eines Dateityps dynamisch Symbole zuweisen können. Jedes Mal, wenn eine Datei des Typs angezeigt wird, fragt die Shell den Handler nach dem entsprechenden Symbol ab. Beispielsweise kann ein Symbol Handler verschiedenen Membern des Dateityps verschiedene Symbole zuweisen oder das Symbol basierend auf dem aktuellen Status der Datei variieren.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Symbol Handler spezifisch sind.

-   [Implementieren von Symbol Handlern](#step-1-implementing-icon-handlers)
-   [Implementieren der iextracticon-Schnittstelle](#step-2-implementing-the-iextracticon-interface)
-   [Registrieren von Symbol Handlern](#step-3-registering-icon-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-icon-handlers"></a>Schritt 1: Implementieren von Symbol Handlern

Wie bei allen Shellerweiterungs Handlern sind Symbol Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)müssen beide Schnittstellen exportiert werden: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

Die Shell initialisiert den Handler über seine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle. Diese Schnittstelle wird verwendet, um den Klassen Bezeichner (CLSID) des Handlers anzufordern und den Dateinamen bereitzustellen. Der Rest des Vorgangs erfolgt über die [**iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) -Schnittstelle. Eine allgemeine Erörterung der Implementierung von Shellerweiterungs Handlern, einschließlich der **IPersistFile** -Schnittstelle, finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md). Im restlichen Teil dieses Dokuments wird erläutert, wie die **iextracticon** -Schnittstelle implementiert wird.

### <a name="step-2-implementing-the-iextracticon-interface"></a>Schritt 2: Implementieren der iextracticon-Schnittstelle

Nachdem die Schnittstelle initialisiert wurde, verwendet die Shell die [**iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) -Schnittstelle des Handlers, um das entsprechende Symbol anzufordern. Die Schnittstelle verfügt über zwei Methoden: [**iextracticon:: getikonlocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) und [**iextracticon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract).

Symbole werden durch ihren Speicherort im Dateisystem identifiziert. Die [**iextracticon:: getikonlocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) -Methode wird aufgerufen, um diese Informationen anzufordern. Legen Sie den Parameter " *sziconfile* " auf den Dateinamen fest. Wenn mehr als ein Symbol in der Datei vorhanden ist, legen Sie *piindex* auf den Index des Symbols fest. Weisen Sie den beiden Flag-Variablen entsprechende Werte zu. Wenn Sie keinen Dateinamen angeben möchten oder wenn Sie nicht möchten, dass die Shell das Symbol extrahiert, legen Sie das Flag " **Gil \_ notfilename** " im *PWFLAGS* -Parameter fest. Sie müssen " *sziconfile*" keinen Wert zuweisen, aber der Handler muss Symbol Handles bereitstellen, wenn die Shell " [**iextracticon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)" aufruft.

Wenn Sie einen Dateinamen zurückgeben, versucht die Shell normalerweise, das Symbol aus dem Cache zu laden. Um das Laden eines zwischengespeicherten Symbols zu verhindern, legen Sie das Flag " **Gil \_ DontCache** " im *PWFLAGS* -Parameter fest. Wenn ein zwischengespeichertes Symbol nicht geladen wird, ruft die Shell [**iextracticon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) auf, um das Symbol Handle anzufordern.

Wenn eine Datei und ein Index von [**iextracticon:: getikonlocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation)angegeben wurden, werden Sie in den Parametern *pszFile* bzw. *nidinindex* an [**iextracticon:: Extract**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) übergeben. Wenn ein Dateiname angegeben wird, kann der Handler S false zurückgeben, damit \_ die Shell das Symbol extrahiert. Andernfalls muss Ihr Handler große und kleine Symbole extrahieren oder anderweitig extrahieren und die HICON-Handles den Parametern " *phifilarge* " und " *phikonsmall* " zuweisen. Die Shell fügt die Symbole in Ihren Cache ein, um nachfolgende Aufrufe des Handlers zu beschleunigen.

### <a name="step-3-registering-icon-handlers"></a>Schritt 3: Registrieren von Symbol Handlern

Wenn Sie [ein Symbol](icon.md) für einen [Dateityp](fa-file-types.md)statisch registrieren, erstellen Sie einen **DefaultIcon** -Unterschlüssel unter der ProgID für den Dateityp. Der Standardwert wird auf die Datei festgelegt, die das Symbol enthält. Zum Registrieren eines Symbol Handlers müssen Sie immer noch über den Unterschlüssel **DefaultIcon** verfügen, aber der Standardwert muss auf "%1" festgelegt werden. Fügen Sie dem **shellex** -Unterschlüssel des ProgID-unter Schlüssels einen **iconhandler** -Unterschlüssel hinzu, und legen Sie dessen Standardwert auf die Zeichen folgen Form der CLSID-GUID des Handlers fest. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

Im folgenden Beispiel wird der Registrierungs Eintrag durch [Anpassen von Symbolen](icon.md) geändert, sodass der MYP-Dateityp nun anstelle eines statisch definierten Symbols einen Kontextmenü Handler verwendet.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Shellerweiterungshandlern](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**Iextracticon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
