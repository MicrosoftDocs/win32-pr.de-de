---
title: Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente
description: In diesem Thema werden die standardmäßigen Windows-Steuerelemente beschrieben, die von der Microsoft UI Automation unterstützt werden Vollständige Unterstützung wird nur für Steuerelemente ab Version 6 von ComCtrl32.dll bereitgestellt (verfügbar in Windows XP und höher).
ms.assetid: 4821684c-8a90-413c-8ddc-699926e3bb09
keywords:
- Clients, Unterstützung der Benutzeroberflächen Automatisierung für Standard Steuerelemente
- Clients, Standard Steuerungs Unterstützung
- Clients, Win32-Steuerelemente
- Benutzeroberflächen Automatisierung, Unterstützung für Standard Steuerelemente
- Benutzeroberflächen Automatisierung, Unterstützung von Standard Steuerelementen
- UI-Automatisierung, Win32-Steuerelemente
- Unterstützung für Standardsteuerelemente
- Standard Steuerelement Unterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6e384b9ee0fd72fd8a41aa3f791a5c996fe6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515536"
---
# <a name="ui-automation-support-for-standard-controls"></a>Benutzeroberflächenautomatisierungs-Unterstützung für Standardsteuerelemente

In diesem Thema werden die standardmäßigen Windows-Steuerelemente beschrieben, die von der Microsoft UI Automation unterstützt werden Vollständige Unterstützung wird nur für Steuerelemente ab Version 6 von ComCtrl32.dll bereitgestellt (verfügbar in Windows XP und höher).

> [!Note]  
> Das RichEdit-Steuerelement wird nur für Versionen unterstützt, die mit Windows Vista ausgeliefert wurden (in RichEd20.dll Version 3,1 und höher sowie MsftEdit.dll Version 4,1 und höher).

 

In der folgenden Tabelle werden die Klassennamen der unterstützten Standard Steuerelemente zusammen mit den entsprechenden Steuerelement Typen der Benutzeroberflächen Automatisierung aufgelistet.



| Klassenname          | Steuerelementtyp        |
|---------------------|---------------------|
| Schaltfläche              | Schaltfläche              |
| Schaltfläche              | RadioButton         |
| Schaltfläche              | Gruppieren               |
| Schaltfläche              | CheckBox            |
| Schaltfläche              | Hyperlink           |
| Schaltfläche              | SplitButton         |
| Schaltfläche              | CheckBox            |
| ComboBoxEx32        | Kombinationsfeld            |
| Kombinationsfeld            | Kombinationsfeld            |
| Bearbeiten                | Dokument            |
| Bearbeiten                | Bearbeiten                |
| SysLink             | Hyperlink           |
| statischen              | Text                |
| statischen              | Image               |
| SysIPAddress32      | Benutzerdefiniert              |
| SysHeader32         | Header/HeaderItem   |
| SysListView32       | DataGrid            |
| SysListView32       | List                |
| ListBox             | List                |
| ListBox             | ListItem            |
| \#32768             | Menü                |
| \#32768             | MenuItem            |
| msctls \_ progress32  | ProgressBar         |
| RichEdit            | Dokument. Siehe Hinweis. |
| RichEdit20A         | Dokument            |
| RichEdit20W         | Dokument            |
| RichEdit50W         | Dokument            |
| ScrollBar           | Schieberegler              |
| msctls \_ trackbar32  | Schieberegler              |
| msctls \_ updown32    | Spinner             |
| msctls \_ statusbar32 | StatusBar           |
| SysTabControl32     | Registerkarte                 |
| SysTabControl32     | TabItem             |
| ToolbarWindow32     | ToolBar             |
| ToolbarWindow32     | MenuItem            |
| ToolbarWindow32     | Schaltfläche              |
| ToolbarWindow32     | CheckBox            |
| ToolbarWindow32     | RadioButton         |
| ToolbarWindow32     | Trennzeichen           |
| Quick Infos \_ class32   | ToolTip             |
| \#32774             | ToolTip             |
| ReBarWindow32       | Symbolleiste             |
| SysTreeView32       | Struktur                |
| SysTreeView32       | TreeItem            |



 

Die in der folgenden Tabelle aufgeführten Steuerelemente werden nicht unterstützt.



| Klassenname                                    | Steuerelementtyp |
|-----------------------------------------------|--------------|
| SysAnimate32                                  | Image        |
| SysPager                                      | Spinner      |
| SysDateTimePick32                             | Benutzerdefiniert       |
| SysMonthCal32                                 | Kalender     |
| MS \_ winnote                                   | QuickInfo      |
| VBBubble                                      | QuickInfo      |
| ScrollBar (wenn als eigenständiges Steuerelement verwendet) | Schieberegler       |
| SuperGrid                                     | Benutzerdefiniert       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Steuerelementtypen für Benutzeroberflächenautomatisierung](uiauto-controltypesoverview.md)
</dt> </dl>

 

 




