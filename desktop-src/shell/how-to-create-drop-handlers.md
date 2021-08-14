---
description: Implementieren und Registrieren eines Abbruchhandlers.
title: Erstellen von Abbruchhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34c06aa3eae1892b5b86ce3a0f3b1198be41cd2f9dda5c9bd0956b40a53146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223584"
---
# <a name="how-to-create-drop-handlers"></a>Erstellen von Abbruchhandlern

Standardmäßig sind Dateien keine Abbruchziele. Sie können die Member eines Dateityps [zu](fa-file-types.md) Abbruchzielen machen, indem Sie einen Abbruchhandler *implementieren und registrieren.*

Wenn ein Abbruchhandler für einen Dateityp registriert ist, wird er immer dann aufgerufen, wenn ein Objekt auf einen Member des Dateityps gezogen oder gelöscht wird. Die Shell verwaltet den Vorgang, indem die entsprechenden Methoden für die [**IDropTarget-Schnittstelle**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) des Handlers aufgerufen werden.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shell-Erweiterungshandlers werden unter [Creating Shell Extension Handlers (Erstellen von Shellerweiterungshandlern) erläutert.](handlers.md) Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Abbruchhandler spezifisch sind.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implementing-drop-handlers"></a>Schritt 1: Implementieren von Abbruchhandlern

Wie alle Shell-Erweiterungshandler sind Abbruchhandler In-Process-Component Object Model (COM)-Objekte, die als DLLs implementiert sind. Sie exportieren zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)zwei Schnittstellen: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).

Die Shell initialisiert den Handler über die [**IPersistFile-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Sie verwendet diese Schnittstelle, um den Klassenbezeichner (CLSID) des Handlers an fordern und mit dem Namen der Datei zur Verfügung zu stellen. Eine allgemeine Erörterung der Implementierung von Shell-Erweiterungshandlern, einschließlich der **IPersistFile-Schnittstelle,** finden Sie unter [Creating Shell Extension Handlers](handlers.md).

Nachdem der Abbruchhandler initialisiert wurde, ruft die Shell die entsprechende Methode auf der [**IDropTarget-Schnittstelle des Handlers**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) auf.

### <a name="step-2-registering-drop-handlers"></a>Schritt 2: Registrieren von Abbruchhandlern

Abbruchhandler werden unter dem Unterschlüssel dieses Dateityps registriert.

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

Erstellen Sie einen Unterschlüssel **von DropHandler** mit dem Namen für den Handler, und legen Sie den Standardwert des Unterschlüssels auf die Zeichenfolgenform der CLSID-GUID des Handlers fest. Eine allgemeine Erörterung des Registrierens von Shell-Erweiterungshandlern finden Sie unter [Creating Shell Extension Handlers](handlers.md).

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Abbruchhandler für einen .myp-Beispieldateityp aktivieren.

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

[**Idroptarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
