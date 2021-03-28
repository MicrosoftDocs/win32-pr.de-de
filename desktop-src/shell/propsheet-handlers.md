---
description: Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt klickt, enthält das Kontextmenü, das normalerweise angezeigt wird, normalerweise ein Eigenschaften Element.
title: Eigenschaften Blatt Handler
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866151"
---
# <a name="property-sheet-handlers"></a>Eigenschaften Blatt Handler

Wenn ein Benutzer mit der rechten Maustaste auf ein Shellobjekt klickt, enthält das Kontextmenü, das normalerweise angezeigt wird, normalerweise ein **Eigenschaften** Element. Wenn Sie dieses Element auswählen, wird ein Eigenschaften Blatt gestartet, das es dem Benutzer ermöglicht, die Eigenschaften des Objekts anzuzeigen und in einigen Fällen zu ändern. Sie können dieses Eigenschaften Blatt anpassen, indem Sie einen *Eigenschaften Blatt Handler* implementieren und registrieren.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Eigenschaften Blatt Handler spezifisch sind.

-   [Funktionsweise von Eigenschaften Blatt Handlern](#how-property-sheet-handlers-work)
-   [Registrieren und Implementieren eines Eigenschaften Blatt Handlers für ein bereitgestelltes Laufwerk](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [Zugehörige Themen](#related-topics)

## <a name="how-property-sheet-handlers-work"></a>Funktionsweise von Eigenschaften Blatt Handlern

Die folgende Abbildung zeigt das Eigenschaften Blatt "Eigenschaften" für eine Windows XP-Textdatei.

![Eigenschaften Blatt](images/propsheethandler1.jpg)

Diese Abbildung zeigt das Eigenschaften Blatt für Standardeigenschaften, das für jede Datei angezeigt wird. Für viele dieser Eigenschaften Blätter können Sie dem Eigenschaften Blatt eine oder mehrere Seiten hinzufügen, indem Sie einen Eigenschaften Blatt Handler implementieren und registrieren.

Eigenschaften Blatt Handler werden am häufigsten für einen [Dateityp](fa-file-types.md)registriert. Jeder Handler kann dem Eigenschaften Blatt Eigenschaften für die Klasse eine benutzerdefinierte Seite hinzufügen. Diese Seiten geben Benutzern in der Regel Zugriff auf Eigenschaften, die für den jeweiligen Dateityp spezifisch sind. Ein Dateityp, der aus Textdokumenten besteht, könnte z. b. eine Seite anzeigen, auf der Titel und Autor aufgelistet sind, sowie eine abstrakte des Dokuments. Ein Sonderfall dieses Typs eines Eigenschaften Blatt Handlers wird verwendet, um dem Eigenschaften Blatt Eigenschaften für ein bereitgestelltes Laufwerk eine Seite hinzuzufügen.

Die andere Verwendung für Eigenschaften Blatt Handler ist das Ersetzen von Seiten in den Eigenschaften Blättern, die von System Steuerungsanwendungen angezeigt werden. Ein Maus Hersteller kann z. b. einen Eigenschaften Blatt Handler verwenden, um die **Schalt** Flächen Seite auf dem Eigenschaften Blatt für die **Maus Eigenschaften** der Systemsteuerung durch eine Seite zu ersetzen, die für die Merkmale der Maus angepasst ist.

Wie bei allen Shellerweiterungs Handlern sind Eigenschaften Blatt Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)müssen beide Schnittstellen exportiert werden: [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).

Die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -Schnittstelle wird von der Shell verwendet, um den Handler zu initialisieren. Wenn die Shell [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)aufruft, übergibt Sie ein Datenobjekt mit dem Namen des Objekts und den Zeiger auf eine Element Bezeichner-Liste (PIDL) des Ordners, der die Datei enthält. Der *hregkey* -Parameter wird nicht mit Eigenschaften Blatt Handlern verwendet. Die **ishellextinit:: Initialize** -Methode muss den Dateinamen aus dem Datenobjekt extrahieren und den Namen und die PIDL des Ordners für die spätere Verwendung speichern. Weitere Informationen finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md)im Abschnitt *Implementieren von ishellextinit* .

Der Rest des Vorgangs erfolgt über die [**ishellpropsheetext**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) -Schnittstelle des Handlers. Wenn das Eigenschaften Blatt einem Dateityp zugeordnet ist, ruft die Shell [**ishellpropsheetext:: addPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) auf, damit der Handler dem Eigenschaften Blatt eine Seite hinzufügen kann. Wenn das Eigenschaften Blatt einer System Steuerungsanwendung zugeordnet ist, ruft die Shell [**ishellpropsheetext:: replacepage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) auf, damit der Handler eine Seite ersetzen kann.

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a>Registrieren und Implementieren eines Eigenschaften Blatt Handlers für ein bereitgestelltes Laufwerk

Jedes eingebundene Laufwerk verfügt über ein Eigenschaften Blatt, das vom Benutzer angezeigt werden kann. In der folgenden Abbildung ist ein Eigenschaften Blatt für die Eigenschaften eines CD-ROM-Laufwerks dargestellt.

![Eigenschaften Blatt "CD-ROM-Eigenschaften"](images/propsheethandler2.jpg)

Es gibt eine Vielzahl von Geräten, die als Laufwerke bereitgestellt werden können. Da das Standardeigenschaften Blatt, das für Laufwerke konzipiert ist, bei manchen Geräten möglicherweise nicht ausreicht, kann ein Eigenschaften Blatt Handler implementiert werden, um eine Seite hinzuzufügen, die für das bereitgestellte Gerät spezifisch ist. Die grundlegende Implementierung dieses Typs von Eigenschaften Blatt Handlers ist identisch mit dem, der unter [registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)mit zwei Ausnahmen erläutert wird.

-   Das Datenobjekt, das an die [**ishellextinit:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode des Handlers übermittelt wird, kann den Laufwerks Pfad im [cfstr \_ mountedvolume](clipboard.md) -Format anstelle des [CF- \_ HDROP](clipboard.md) -Formats enthalten. Das CF- \_ HDROP-Format wird verwendet, wenn das Gerät in einen Laufwerk Buchstaben eingebunden wird. Das Format cfstr \_ mountedvolume wird mit NTFS-Dateisystemen verwendet, wenn das Remote Gerät in einen Ordner und nicht in einen Laufwerk Buchstaben eingebunden wird.
-   Die GUID des Handlers wird unter dem **HKEY \_ - \_ Klassen** Stamm \\ **Laufwerk** \\ **shellex** \\ **propertysheethandlers** Key registriert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren und Implementieren eines Eigenschaften Blatt Handlers für einen Dateityp](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[Registrieren und Implementieren eines Eigenschaften Blatt Handlers für eine System Steuerungsanwendung](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 
