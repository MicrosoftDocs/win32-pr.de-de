---
description: Vorgehensweise beim Implementieren und Registrieren eines Drop-Handlers.
title: Erstellen von Drop-Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215944"
---
# <a name="how-to-create-drop-handlers"></a>Erstellen von Drop-Handlern

Standardmäßig handelt es sich bei Dateien nicht um Drop-Ziele. Sie können die Member eines [Dateityps](fa-file-types.md) in Ablage Ziele ändern, indem Sie einen *Drop-Handler* implementieren und registrieren.

Wenn ein Drop-Handler für einen Dateityp registriert ist, wird er immer dann aufgerufen, wenn ein Objekt auf einen Member des Dateityps gezogen oder gelöscht wird. Die Shell verwaltet den Vorgang, indem die entsprechenden Methoden in der [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Handlers aufgerufen werden.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Drop-Handler spezifisch sind.

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-drop-handlers"></a>Schritt 1: Implementieren von Drop-Handlern

Wie bei allen Shellerweiterungs Handlern sind Drop-Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)werden zwei Schnittstellen exportiert: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Die Shell initialisiert den Handler über seine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle. Diese Schnittstelle wird verwendet, um den Klassen Bezeichner (CLSID) des Handlers anzufordern und den Dateinamen bereitzustellen. Eine allgemeine Erörterung der Implementierung von Shellerweiterungs Handlern, einschließlich der **IPersistFile** -Schnittstelle, finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

Nachdem der Drop-Handler initialisiert wurde, ruft die Shell die entsprechende Methode für die [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle des Handlers auf.

### <a name="step-2-registering-drop-handlers"></a>Schritt 2: Registrieren von Drop-Handlern

Drop Handler werden unter dem Unterschlüssel dieses Dateityps registriert.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Erstellen Sie einen Unterschlüssel von **drophandler** mit dem Namen für den Handler, und legen Sie den Standardwert des unter Schlüssels auf die Zeichen folgen Form der CLSID-GUID des Handlers fest. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Drop-Handler für einen example. MYP-Dateityp aktivieren.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Shellerweiterungshandlern](handlers.md)
</dt> <dt>

[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
