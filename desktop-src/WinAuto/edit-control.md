---
title: Edit-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)
description: Mit Steuerelementen bearbeiten können Benutzer Text anzeigen und bearbeiten.
ms.assetid: a42c73f2-4005-4db9-84bc-637c9c4310f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dde6e562b651b91376bc7d675b2b71ac999cf48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516100"
---
# <a name="edit-control-msaa-ui-element-reference"></a>Edit-Steuer Element (MSAA-Benutzeroberflächen Element-Referenz)

> [!Note]  
> In diesem Thema wird das **Bearbeiten von Steuer** Element Objekten für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise zum Erstellen von **Bearbeitungs Steuerungs** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Mit Steuerelementen bearbeiten können Benutzer Text anzeigen und bearbeiten. Bearbeitungs Steuerelemente werden mit vielen verschiedenen Stilen erstellt, z \_ . b. mehreren Zeilen. Dieser Stil erstellt ein mehrzeilige Bearbeitungs Steuerelement, z. b. den Client Bereich von Notepad, und es ist schreibgeschützt \_ , wodurch ein Schreib geschütztes Bearbeitungs Steuerelement erstellt wird.

Microsoft Active Accessibility unterscheidet nicht zwischen Bearbeitungs Steuerelementen, die mit dem Fenster Klassennamen "Edit" erstellt wurden, und Rich Edit-Steuerelementen, die mit dem Fenster Klassennamen "RichEdit" oder "RichEdit20A" erstellt wurden.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Bearbeitungs Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Bearbeitungs Steuerelemente unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Die **KeyboardShortcut** -Eigenschaft ist die Zugriffstaste des Bearbeitungs Steuer Elements, bei der es sich um ein unterstrichenes Zeichen im Text der Bezeichnung des Bearbeitungs Steuer Elements handelt. Beispielsweise wird in einem Standard Dialogfeld zum Öffnen von Dateien, z. b. in WordPad, **KeyboardShortcut** für das Bearbeitungs Steuerelement mit der Bezeichnung "Dateiname:" alt + n angezeigt.                                                                                                                                                                                                                                                                                                                                        |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft ist der Text aus einem statischen Text Steuerelement, das das Bearbeitungs Steuerelement bezeichnet. Beispielsweise ist die **Name** -Eigenschaft für das Bearbeitungs Steuerelement in einem Standard Dialogfeld zum Öffnen von Dateien, z. b. in WordPad, "Dateiname:".                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | Die über **geordnete** Eigenschaft ist ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Steuerelement umgibt und die gleiche **Name** -Eigenschaft und den Fenster Klassennamen wie das Steuerelement aufweist.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist ein [**\_ \_ Text des Rollen Systems**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**\_Zugriffs Auswahl**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System-Integritäts orientiertes Zustands System [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ fokussierbar**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) Zustands System mit Fokussystem für Schreib geschütztes Zustands System geschütztes Zustands System<br/> |
| [**\_accValue erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Die **value** -Eigenschaft ist eine einzelne Zeichenfolge, die den Text im Bearbeitungs Steuerelement enthält. Wenn das Steuerelement jedoch Kenn Wort geschützt ist, gibt die **value** -Eigenschaft E \_ AccessDenied zurück. Für mehrzeilige Bearbeitungs Steuerelemente enthält die Zeichenfolge ein Wagen Rücklauf Zeichen und ein Zeilenumbruch Zeichen am Ende jeder Zeile.                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notizen

-   Microsoft Active Accessibility unterstützt nicht die Auswahl des Texts, der in Edit-und Rich Edit-Steuerelementen enthalten ist, da der Text als Zeichenfolge in der **value** -Eigenschaft des Objekts verfügbar gemacht wird.
-   Das Rich Edit-Steuerelement, das von Riched20.dll bereitgestellt wird (das in Text-Editoren wie WordPad in Windows 98 verwendet wird), sendet keine WinEvents, wenn die Position der Einfügemarke während der Textauswahl geändert wird. Wenn Benutzer die UMSCHALTTASTE und die Pfeiltasten drücken, um Text auszuwählen, löst das Caretzeichen Objekt das [**Ereignis \_ Objekt \_ locationchange**](event-constants.md) WinEvent nicht aus. Wenn die Auswahlprogramm gesteuert durch umfassende Bearbeitungs Nachrichten festgelegt wird, sendet das Caretzeichen-Objekt keine Ereignisse, um die neue Position anzugeben.

    Alle Anwendungen, die Riched20.dll verwenden, weisen dieses Problem auf. Anwendungen, die frühere Versionen des Rich Edit-Steuer Elements verwenden, senden Ereignisse auf der Grundlage der Auswahl ordnungsgemäß.

-   Der **Status** Wert für Steuerelemente zur Kenn Wort Bearbeitung schließt immer das Bitflag " [**State \_ System \_ Protected**](object-state-constants.md)" ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





