---
title: Implementieren des COM-Objekts im Kontextmenü
description: Eine Kontextmenüerweiterung ist ein COM-Objekt, das als Prozessserver implementiert wird.
ms.assetid: 362dd8e5-1518-4bf4-ac53-115263cd6c62
ms.tgt_platform: multiple
keywords:
- Kontextmenü COM-Objekt AD
- 'Kontextmenü: COM-Objekt AD, Implementieren'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ac371ea64239c18de2a8f30c969eb6d920221f0a802f18ceeebfef2c3991e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187648"
---
# <a name="implementing-the-context-menu-com-object"></a>Implementieren des COM-Objekts im Kontextmenü

Eine Kontextmenüerweiterung ist ein COM-Objekt, das als Prozessserver implementiert wird. Die Kontextmenüerweiterung muss die Schnittstellen [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) und [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) implementieren. Eine Kontextmenüerweiterung wird instanziiert, wenn der Benutzer das Kontextmenü für ein Objekt einer Klasse anzeigt, für das die Kontextmenüerweiterung registriert wurde.

## <a name="implementing-ishellextinit"></a>Implementieren von IShellExtInit

Nachdem das COM-Objekt der Kontextmenüerweiterung instanziiert wurde, wird die [**IShellExtInit::Initialize-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) aufgerufen. **IShellExtInit::Initialize** stellt die Kontextmenüerweiterung mit einem [**IDataObject-Objekt**](/windows/win32/api/objidl/nn-objidl-idataobject) bereit, das Daten enthält, die für das Verzeichnisobjekt relevant sind, für das das Kontextmenü gilt.

Das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält Daten im [**CFSTR \_ DSOBJECTNAMES-Format.**](/previous-versions/windows/desktop/mmc/cfstr-dsobjectnames-clipboard-format) Das **CFSTR \_ DSOBJECTNAMES-Datenformat** ist ein **HGLOBAL-Objekt,** das eine [**DSOBJECTNAMES-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) enthält. Die **DSOBJECTNAMES-Struktur** enthält Daten über das Verzeichnisobjekt, für das die Eigenschaftenblatterweiterung gilt.

Das [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) enthält auch Daten im [**FORMAT CFSTR \_ DS DISPLAY SPEC \_ \_ \_ OPTIONS.**](cfstr-ds-display-spec-options.md) Das **CFSTR \_ DS \_ DISPLAY SPEC \_ \_ OPTIONS-Datenformat** ist ein **HGLOBAL-Format,** das eine [**DSDISPLAYSPECOPTIONS-Struktur**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) enthält. **DSDISPLAYSPECOPTIONS** enthält Konfigurationsdaten für die Verwendung durch die Erweiterung.

Wenn von [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)ein anderer Wert als **S \_ OK** zurückgegeben wird, wird die Kontextmenüerweiterung nicht verwendet.

Die Parameter *pidlFolder* und *hkeyProgID* der [**IShellExtInit::Initialize-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) werden nicht verwendet.

## <a name="implementing-icontextmenu"></a>Implementieren von IContextMenu

Nachdem [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) zurückgegeben wurde, wird die [**IContextMenu::QueryContextMenu-Methode**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) aufgerufen, um die Menüelemente abzurufen, die von der Kontextmenüerweiterung hinzugefügt werden. Die **QueryContextMenu-Implementierung** ist recht einfach. Die Kontextmenüerweiterung fügt ihre Menüelemente mithilfe der [**InsertMenuItem-Funktion**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) oder einer ähnlichen Funktion hinzu. Die Menübefehlsbezeichner müssen größer oder gleich *idCmdFirst* und kleiner als *idCmdLast* sein. **QueryContextMenu** muss den größten numerischen Bezeichner zurückgeben, der dem Menü plus 1 hinzugefügt wurde. Die beste Möglichkeit zum Zuweisen von Menübefehlsbezeichnern besteht darin, bei null zu beginnen und nacheinander zu arbeiten. Wenn die Kontextmenüerweiterung keine Menüelemente benötigen, sollte sie dem Menü einfach keine Elemente hinzufügen und 0 (null) von **QueryContextMenu** zurückgeben.

[**IContextMenu::GetCommandString**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) wird aufgerufen, um Textdaten für das Menüelement abzurufen, z. B. Hilfetext, der für das Menüelement angezeigt werden soll. Es ist möglich, dass der Kontextmenühost Unicode-Zeichenfolgen verwendet, während die Erweiterung ANSI-Zeichenfolgen verwendet. Aus diesem Grund müssen die **GCS \_ HELPTEXTA-,** **GCS \_ HELPTEXTW-,** **GCS \_ VERBA-** und **GCS \_ VERBW-Fälle** einzeln behandelt werden. Die Implementierung dieser Methode ist optional.

[**IContextMenu::InvokeCommand**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) wird aufgerufen, wenn eines der von der Kontextmenüerweiterung installierten Menüelemente ausgewählt ist. Das Kontextmenü führt die gewünschten Aktionen als Reaktion auf diese Methode aus oder initiiert sie.

 

 