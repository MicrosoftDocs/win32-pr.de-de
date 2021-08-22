---
description: Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, enthält das angezeigte Kontextmenü normalerweise ein Eigenschaftenelement.
title: Eigenschaftenblatthandler
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 27327db4718430ba646d9566227116e304d4d5f5770d0119987b32e0cd2adce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719542"
---
# <a name="property-sheet-handlers"></a>Eigenschaftenblatthandler

Wenn ein Benutzer mit der rechten Maustaste auf ein Shell-Objekt klickt, enthält das angezeigte Kontextmenü normalerweise ein **Eigenschaftenelement.** Wenn Sie dieses Element auswählen, wird ein Eigenschaftenblatt gestartet, mit dem der Benutzer die Eigenschaften des Objekts anzeigen und in einigen Fällen ändern kann. Sie können dieses Eigenschaftenblatt anpassen, indem Sie einen *Eigenschaftenblatthandler* implementieren und registrieren.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungshandlers werden unter [Erstellen von Shellerweiterungshandlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die spezifisch für Eigenschaftenblatthandler sind.

-   [Funktionsweise von Eigenschaftenblatthandlern](#how-property-sheet-handlers-work)
-   [Registrieren und Implementieren eines Eigenschaftenblatthandlers für ein eingebundenes Laufwerk](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Zugehörige Themen](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Funktionsweise von Eigenschaftenblatthandlern

Die folgende Abbildung zeigt das Eigenschaftenblatt für eine Windows XP-Textdatei.

![Eigenschaftenblatt](images/propsheethandler1.jpg)

Diese Abbildung zeigt das Standardeigenschaftenblatt, das für jede Datei angezeigt wird. Bei vielen solchen Eigenschaftenblättern können Sie dem Eigenschaftenblatt eine oder mehrere Seiten hinzufügen, indem Sie einen Eigenschaftenblatthandler implementieren und registrieren.

Eigenschaftenblatthandler werden am häufigsten für einen [Dateityp](fa-file-types.md)registriert. Jeder Handler kann dem Eigenschaftenblatt Eigenschaften für die Klasse eine benutzerdefinierte Seite hinzufügen. Diese Seiten gewähren Benutzern in der Regel Zugriff auf Eigenschaften, die für den jeweiligen Dateityp spezifisch sind. Ein Dateityp, der aus Textdokumenten besteht, kann z. B. eine Seite anzeigen, die den Titel und den Autor sowie eine Zusammenfassung des Dokuments auflistet. Ein Sonderfall dieses Eigenschaftenblatthandlertyps wird verwendet, um dem Eigenschafteneigenschaftenblatt für ein eingebundenes Laufwerk eine Seite hinzuzufügen.

Die andere Verwendung für Eigenschaftenblatthandler besteht darin, Seiten in den Eigenschaftenblättern zu ersetzen, die von Systemsteuerung Anwendungen angezeigt werden. Ein Maushersteller kann beispielsweise einen Eigenschaftenblatthandler verwenden, um die Seite **Schaltflächen** auf dem **Eigenschaftenblatt Mauseigenschaften** des Systemsteuerung durch eine Seite zu ersetzen, die an die Merkmale der Maus angepasst ist.

Wie bei allen Shellerweiterungshandlern handelt es sich bei Eigenschaftenblatthandlern um in-process Component Object Model (COM)-Objekte, die als DLLs implementiert werden. Sie müssen zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)zwei Schnittstellen exportieren: [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IShellPropSheetExt.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)

Die [**IShellExtInit-Schnittstelle**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) wird von der Shell verwendet, um den Handler zu initialisieren. Wenn die Shell [**IShellExtInit::Initialize aufruft,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)übergibt sie ein Datenobjekt mit dem Namen des Objekts und den Zeiger auf eine Elementbezeichnerliste (PIDL) des Ordners, der die Datei enthält. Der *hRegKey-Parameter* wird nicht mit Eigenschaftenblatthandlern verwendet. Die **IShellExtInit::Initialize-Methode** muss den Dateinamen aus dem Datenobjekt extrahieren und den Namen und die PIDL des Ordners zur späteren Verwendung speichern. Weitere Informationen finden Sie im Abschnitt *Implementing IShellExtInit (Implementieren von IShellExtInit)* unter [Creating Shell Extension Handlers (Erstellen von Shellerweiterungshandlern).](handlers.md)

Der Rest des Vorgangs erfolgt über die [**IShellPropSheetExt-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) des Handlers. Wenn das Eigenschaftenblatt einem Dateityp zugeordnet ist, ruft die Shell [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) auf, damit der Handler dem Eigenschaftenblatt eine Seite hinzufügen kann. Wenn das Eigenschaftenblatt einer Systemsteuerung Anwendung zugeordnet ist, ruft die Shell [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) auf, damit der Handler eine Seite ersetzen kann.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrieren und Implementieren eines Eigenschaftenblatthandlers für ein eingebundenes Laufwerk

Jedes bereitgestellte Laufwerk verfügt über ein Eigenschaftenblatt, das vom Benutzer angezeigt werden kann. Die folgende Abbildung zeigt ein Eigenschaftenblatt für ein CD-ROM-Laufwerk.

![Eigenschaftenblatt "cd-rom"](images/propsheethandler2.jpg)

Es gibt eine Vielzahl von Geräten, die als Laufwerke eingebunden werden können. Da das Standardeigenschaftenblatt, das für Datenträgerlaufwerke entworfen wurde, für einige Geräte möglicherweise nicht ausreicht, kann ein Eigenschaftenblatthandler implementiert werden, um eine Seite hinzuzufügen, die spezifisch für das eingebundene Gerät ist. Die grundlegende Implementierung dieses Eigenschaftenblatthandlertyps ist mit der unter [Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)beschriebenen identisch, mit zwei Ausnahmen.

-   Das Datenobjekt, das an die [**IShellExtInit::Initialize-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) des Handlers übergeben wird, kann den Laufwerkspfad im [CFSTR \_ MOUNTEDVOLUME-Format](clipboard.md) anstelle des [CF \_ HDROP-Formats](clipboard.md) enthalten. Das CF \_ HDROP-Format wird verwendet, wenn das Gerät in einen Laufwerkbuchstaben eingebunden wird. Das CFSTR \_ MOUNTEDVOLUME-Format wird mit NTFS-Dateisystemen verwendet, wenn das Remotegerät in einen Ordner und nicht in einen Laufwerkbuchstaben eingebunden wird.
-   Die GUID des Handlers wird unter dem **Schlüssel HKEY \_ CLASSES \_ ROOT** \\ **Drive** \\ **shellex** \\ **PropertySheetHandlers** registriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren und Implementieren eines Eigenschaftenblatthandlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Registrieren und Implementieren eines Eigenschaftenblatthandlers für eine Systemsteuerung-Anwendung](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
