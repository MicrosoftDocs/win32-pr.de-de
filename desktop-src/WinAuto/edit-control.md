---
title: Steuerelement bearbeiten (Referenz zum MSAA-UI-Element)
description: Mit Steuerelementen bearbeiten kann ein Benutzer Text anzeigen und bearbeiten.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3844dcdf99f925813765ae46494b0ff70345c086f3845304fff0e53d70f07d22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829844"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Steuerelement bearbeiten (Referenz zum MSAA-UI-Element)

> [!Note]  
> In diesem Thema wird edit Control objects for purposes of MSAA UI Element Reference (Bearbeiten von **Steuerelementobjekten** für die MSAA-Benutzeroberflächenelementreferenz) beschrieben. Das Erstellen von **Steuerelementobjekten** bearbeiten in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenzdokumentation für das benutzeroberflächenframework, das Sie verwenden.

 

Mit Steuerelementen bearbeiten kann ein Benutzer Text anzeigen und bearbeiten. Bearbeitungssteuerelemente werden mit vielen verschiedenen Stilen wie ES \_ MULTILINE erstellt. Mit diesem Stil wird ein mehrlinebasiertes Bearbeitungssteuer steuerelement erstellt, z. B. der Clientbereich von Editor, und ES READONLY, das ein \_ schreibgeschütztes Bearbeitungssteuerteil erstellt.

Microsoft Active Accessibility unterscheidet nicht zwischen Bearbeitungssteuerelementen, die mit dem Fensterklassennamen "EDIT" erstellt wurden, und rich edit-Steuerelementen, die mit dem Fensterklassennamen "RichEdit" oder "RichEdit20A" erstellt wurden.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Bearbeitungssteuerelemente unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Bearbeitungssteuerelemente unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut-Eigenschaft** ist die Zugriffsschlüssel des Bearbeitungssteuerfelds, bei dem es sich um ein unterstrichenes Zeichen im Text der Bezeichnung des Bearbeitungssteuerfelds handelt. In einem Standarddialogfeld zum Öffnen von Dateien, z. B. in WordPad, ist **"KeyboardShortcut"** für das Bearbeitungssteuerfeld mit der Bezeichnung "Dateiname:" "Alt+n".                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** ist der Text aus einem statischen Textsteuerfeld, das das Bearbeitungssteuerfeld bezeichnet. In einem Standarddialogfeld zum Öffnen von Dateien, z. B. in WordPad, ist die **Name-Eigenschaft** für das Bearbeitungssteuerfeld beispielsweise "Dateiname:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die **Parent-Eigenschaft** ist ein Fenster ( [**ROLE SYSTEM \_ \_ WINDOW**](object-roles.md) ), das das Steuerelement umschließt und über die gleiche **Name-Eigenschaft** und den gleichen Fensterklassennamen wie das -Steuerelement verfügt.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ TEXT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus mindestens einem der folgenden [Werte:](object-state-constants.md)STATE [**SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ READONLY**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ PROTECTED**](object-state-constants.md) \| [**STATE \_ SYSTEM \_ NORMAL**](object-state-constants.md)<br/> |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **Value-Eigenschaft** ist eine einzelne Zeichenfolge, die den Text im Bearbeitungssteuerfeld enthält. Wenn das Steuerelement jedoch kennwortgeschützt ist, gibt **die Value-Eigenschaft** E \_ ACCESSDENIED zurück. Bei Mehrzeilen-Bearbeitungssteuerelementen enthält die Zeichenfolge einen Wagenrücklauf und ein Zeilenumstrich am Ende jeder Zeile.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Hinweise

-   Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Bearbeitungs- und Rich Edit-Steuerelementen enthalten ist, da der Text als Zeichenfolge in der Value-Eigenschaft des Objekts **verfügbar gemacht** wird.
-   Das von Riched20.dll bereitgestellte Rich-Edit-Steuerelement (das in Text-Editoren wie WordPad in Windows 98 verwendet wird) sendet keine WinEvents, wenn die Caretposition während der Textauswahl geändert wird. Wenn Benutzer die UMSCHALTTASTE und die Pfeiltasten drücken, um Text auszuwählen, löst das Caretobjekt das [**Event \_ Object \_ LOCATIONCHANGE**](event-constants.md) WinEvent nicht aus. Wenn die Auswahl programmgesteuert über umfangreiche Bearbeitungsmeldungen festgelegt wird, sendet das Caretobjekt keine Ereignisse, um seine neue Position anzugeben.

    Alle Anwendungen, die Riched20.dll, weisen dieses Problem auf. Anwendungen, die frühere Versionen des Rich-Edit-Steuerelements verwenden, senden Ereignisse basierend auf der Auswahl ordnungsgemäß.

-   Der **Statuswert** für Steuerelemente zur Kennwortbearbeitung enthält immer das [**Bitflag STATE SYSTEM \_ \_ PROTECTED**](object-state-constants.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





