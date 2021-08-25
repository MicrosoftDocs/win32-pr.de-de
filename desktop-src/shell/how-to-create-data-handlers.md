---
description: Erweitern der Zwischenablage mit benutzerdefinierten Datenformathandlern.
title: Erstellen von Datenhandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a3761b4dc8ce3e7d50d967d2267971537d3609e7a7cf76785623734558adac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715050"
---
# <a name="how-to-create-data-handlers"></a>Erstellen von Datenhandlern

Wenn eine Datei in die Zwischenablage kopiert oder gezogen und abgelegt wird, erstellt die Shell ein Datenobjekt, das eine Vielzahl von [Standardformaten für die Zwischenablage](dragdrop.md)unterstützt. Für Dateien mit einem bestimmten Dateityp können Sie die verfügbaren Zwischenablageformate erweitern, indem Sie einen *Datenhandler* implementieren und registrieren. Wenn eine Datei des Dateityps übertragen wird, delegiert die Shell Aufrufe an die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Datenobjekts an den Datenhandler, wenn eines der benutzerdefinierten Formate verwendet wird.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungshandlers werden unter [Erstellen von Shellerweiterungshandlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die spezifisch für Datenhandler sind.

-   [Implementieren von Datenhandlern](#step-1-implementing-data-handlers)
-   [Registrieren von Datenhandlern](#step-2-registering-data-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-implementing-data-handlers"></a>Schritt 1: Implementieren von Datenhandlern

Wie alle Shell-Erweiterungshandler handelt es sich bei Datenhandlern um IN-Process-Component Object Model (COM)-Objekte, die als DLLs implementiert werden. Sie exportieren zwei Schnittstellen zusätzlich zu [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

Die Shell initialisiert den Handler über die [**IPersistFile-Schnittstelle.**](/windows/win32/api/objidl/nn-objidl-ipersistfile) Diese Schnittstelle wird verwendet, um den Klassenbezeichner des Handlers (CLSID) anzufordern, und stellt ihn mit dem Namen der Datei bereit. Eine allgemeine Erläuterung der Implementierung von Shell-Erweiterungshandlern, einschließlich der **IPersistFile-Schnittstelle,** finden Sie unter [Erstellen von Shellerweiterungshandlern.](handlers.md)

Sobald der Datenhandler initialisiert wurde, delegiert die Shell Aufrufe vom Datenobjekt an die [**IDataObject-Schnittstelle**](/windows/win32/api/objidl/nn-objidl-idataobject) des Handlers, wenn eines der benutzerdefinierten Formate verwendet wird.

### <a name="step-2-registering-data-handlers"></a>Schritt 2: Registrieren von Datenhandlern

Datenhandler werden wie hier gezeigt unter dem *ProgID-Unterschlüssel* des Dateityps registriert: **HKEY \_ CLASSES \_ ROOT** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Erstellen Sie unter **DataHandler** einen Unterschlüssel namens für den Handler, und legen Sie den Standardwert des Unterschlüssels dieses Handlers auf die Zeichenfolgenform der CLSID-GUID des Handlers fest. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungshandlern finden Sie unter [Erstellen von Shellerweiterungshandlern.](handlers.md)

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Datenhandler für einen MyP-Beispieldateityp aktivieren.

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
      Shellex
         DataHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Shellerweiterungshandlern](handlers.md)
</dt> <dt>

[**Ipersistfile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**Idataobject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
