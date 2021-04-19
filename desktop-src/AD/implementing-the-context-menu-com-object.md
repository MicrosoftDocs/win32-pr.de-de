---
title: Implementieren des Kontextmenü-com-Objekts
description: Eine Kontextmenüerweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- Kontextmenü-com-Objekt AD
- Kontextmenü-com-Objekt AD, implementieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34d6b487d130327b379ed845f2d0157f2b28056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106339471"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementieren des Kontextmenü-com-Objekts

Eine Kontextmenüerweiterung ist ein COM-Objekt, das als in-proc-Server implementiert wird. Die Kontextmenüerweiterung muss die [**ishellextinit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) -und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) -Schnittstellen implementieren. Eine Kontextmenüerweiterung wird instanziiert, wenn der Benutzer das Kontextmenü für ein Objekt einer Klasse anzeigt, für die die Kontextmenüerweiterung registriert wurde.

## <a name="implementing-ishellextinit"></a>Implementieren von ishellextinit

Nachdem das COM-Objekt der Kontextmenüerweiterung instanziiert wurde, wird die [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode aufgerufen. **Ishellextinit:: Initialize** liefert die Kontextmenüerweiterung mit einem [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) -Objekt, das Daten enthält, die für das Verzeichnis Objekt relevant sind, für das das Kontextmenü gilt.

Das [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält Daten im [**cfstr \_ dsobjectnames**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) -Format. Das Datenformat **cfstr \_ dsobjectnames** ist ein **HGLOBAL** , das eine [**dsobjectnames**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) -Struktur enthält. Die **dsobjectnames** -Struktur enthält Daten über das Verzeichnis Objekt, auf das die Eigenschaften Blatt Erweiterung angewendet wird.

Das [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält auch Daten im Format der Optionen für die [**cfstr \_ DS- \_ Anzeige \_ Spezifikation \_**](cfstr-ds-display-spec-options.md) . Das Datenformat der **cfstr \_ DS- \_ Anzeige \_ \_ Spezifikation** ist ein **HGLOBAL** , das eine [**dsdisplayspecoptions**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) -Struktur enthält. **Dsdisplayspecoptions** enthält Konfigurationsdaten, die von der Erweiterung verwendet werden können.

Wenn ein anderer Wert als **S \_ OK** von [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)zurückgegeben wird, wird die Kontextmenüerweiterung nicht verwendet.

Die Parameter " *pidlfolder* " und " *hkeyprogid* " der [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) -Methode werden nicht verwendet.

## <a name="implementing-icontextmenu"></a>Implementieren von IContextMenu

Nachdem [**ishellextinit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) zurückgegeben wurde, wird die [**IContextMenu:: querycontextmenu**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) -Methode aufgerufen, um die Menü Elemente zu erhalten, die von der Kontextmenüerweiterung hinzugefügt werden. Die **querycontextmenu** -Implementierung ist recht unkompliziert. Die Kontextmenüerweiterung fügt die Menü Elemente mithilfe der [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) -Funktion oder einer ähnlichen Funktion hinzu. Die Menübefehls Bezeichner müssen größer oder gleich *idcmdfirst* sein und müssen kleiner als *idcmdlast* sein. **Querycontextmenu** muss den größten numerischen Bezeichner zurückgeben, der dem Menü plus 1 hinzugefügt wurde. Die beste Möglichkeit, Menübefehls Bezeichner zuzuweisen, besteht darin, bei Null zu beginnen und nacheinander zu arbeiten. Wenn die Kontextmenüerweiterung keine Menü Elemente benötigt, sollten Sie dem Menü einfach keine Elemente hinzufügen und NULL aus **querycontextmenu** zurückgeben.

[**IContextMenu:: getcommandstring**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) wird aufgerufen, um Textdaten für das Menü Element abzurufen, z. b. den Hilfetext, der für das Menü Element angezeigt werden soll. Es ist möglich, dass der Kontextmenü Host Unicode-Zeichen folgen verwendet, während die Erweiterung ANSI-Zeichen folgen verwendet. Aus diesem Grund müssen die Fälle " **GCS \_ helptexta**", " **GCS \_ helptextw**", " **GCS \_ Verba** " und " **GCS \_ verbw** " einzeln behandelt werden. Die Implementierung dieser Methode ist optional.

[**IContextMenu:: InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) wird aufgerufen, wenn eines der von der Kontextmenüerweiterung installierten Menü Elemente ausgewählt wird. Das Kontextmenü führt die gewünschten Aktionen als Reaktion auf diese Methode aus oder initiiert Sie.

 

 