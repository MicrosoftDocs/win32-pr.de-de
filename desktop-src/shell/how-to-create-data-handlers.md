---
description: Erweitern der Zwischenablage mit benutzerdefinierten Datenformat Handlern.
title: Erstellen von Daten Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ecc08769068d975c1fa16ef1385f362c67e43c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994686"
---
# <a name="how-to-create-data-handlers"></a>Erstellen von Daten Handlern

Wenn eine Datei in die Zwischenablage kopiert oder gezogen und abgelegt wird, erstellt die Shell ein Datenobjekt, das eine Vielzahl von standardmäßigen [Zwischenablage Formaten](dragdrop.md)unterstützt. Für Dateien, die einen bestimmten Dateityp haben, können Sie die verfügbaren Zwischenablage Formate durch Implementieren und Registrieren eines *Daten Handlers* erweitern. Wenn eine Datei des Dateityps übertragen wird, delegiert die Shell Aufrufe an die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Datenobjekts an den Daten Handler, wenn eines der benutzerdefinierten Formate verwendet wird.

Die allgemeinen Verfahren zum Implementieren und Registrieren eines Shellerweiterungs Handlers werden unter [Erstellen von Shellerweiterungs Handlern](handlers.md)erläutert. Dieses Dokument konzentriert sich auf die Aspekte der Implementierung, die für Daten Handler spezifisch sind.

-   [Implementieren von Daten Handlern](#step-1-implementing-data-handlers)
-   [Registrieren von Daten Handlern](#step-2-registering-data-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-data-handlers"></a>Schritt 1: Implementieren von Daten Handlern

Wie bei allen Shellerweiterungs Handlern sind Daten Handler in-Process-Component Object Model (com)-Objekten, die als DLLs implementiert werden. Zusätzlich zu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)werden zwei Schnittstellen exportiert: [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) und [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject).

Die Shell initialisiert den Handler über seine [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) -Schnittstelle. Diese Schnittstelle wird verwendet, um den Klassen Bezeichner (CLSID) des Handlers anzufordern und den Dateinamen bereitzustellen. Eine allgemeine Erörterung der Implementierung von Shellerweiterungs Handlern, einschließlich der **IPersistFile** -Schnittstelle, finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

Nachdem der Daten Handler initialisiert wurde, delegiert die Shell Aufrufe aus dem Datenobjekt an die [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Schnittstelle des Handlers, wenn eines der benutzerdefinierten Formate verwendet wird.

### <a name="step-2-registering-data-handlers"></a>Schritt 2: Registrieren von Daten Handlern

Daten Handler werden unter dem *ProgID* -Unterschlüssel des Dateityps registriert, wie hier gezeigt: **HKEY \_ Classes \_ root** \\ *ProgID* \\ **shellex** \\ **DataHandler**

Erstellen Sie einen Unterschlüssel mit dem Namen für den Handler unter **DataHandler** , und legen Sie den Standardwert des unter Schlüssels dieses Handlers auf die Zeichen folgen Form der CLSID-GUID des Handlers fest. Eine allgemeine Erläuterung zum Registrieren von Shellerweiterungs Handlern finden Sie unter [Erstellen von Shellerweiterungs Handlern](handlers.md).

Das folgende Beispiel veranschaulicht Registrierungseinträge, die einen Daten Handler für einen example. MYP-Dateityp aktivieren.

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

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)
</dt> </dl>

 

 
