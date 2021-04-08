---
title: (Dialog Feld) (MSAA-Benutzeroberflächen Element-Referenz)
description: Ein Dialogfeld ist ein temporäres Fenster, das von einer Anwendung zum Abrufen von Benutzereingaben erstellt wird.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727536"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>(Dialog Feld) (MSAA-Benutzeroberflächen Element-Referenz)

> [!Note]  
> In diesem Thema werden **Dialog Feld** Objekte zum Zweck der MSAA-Benutzeroberflächen-Element Referenz beschrieben. Die Vorgehensweise zum Erstellen von **Dialog Feld** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Ein Dialogfeld ist ein temporäres Fenster, das von einer Anwendung zum Abrufen von Benutzereingaben erstellt wird. Eine Anwendung verwendet Dialogfelder, um den Benutzer zur Eingabe zusätzlicher Informationen über Befehle aufzufordern, die der Benutzer aus einem Menü ausgewählt hat. Ein Dialogfeld enthält ein oder mehrere Steuerelemente (untergeordnete Fenster), mit denen der Benutzer Text eingibt, Optionen auswählt oder die Aktion des Befehls steuert.

Der Fenster Klassenname für Dialogfelder lautet " \# 32770".

## <a name="iaccessible-methods"></a>IAccessible-Methoden

In einem Dialogfeld werden die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden unterstützt:



| Methode                                                                    | Kommentare                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Wenn das Dialogfeld eine Standard-pushschaltfläche enthält, ruft die [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) -Methode [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) mit der [**BM \_ -Schalt**](/windows/desktop/Controls/bm-click) Flächen Meldung auf, um auf die Standard Schaltfläche Push zu klicken. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Ein Dialogfeld unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                                 | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | Die **childCount** -Eigenschaft ist gleich der Anzahl der untergeordneten Fenster Steuerelemente im Dialogfeld.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Wenn das Dialogfeld eine Standard Schaltfläche "Push" enthält, ist die **DEFAULTACTION** -Eigenschaft "Press".                                                                                                                                                                                                                                                                                                                                                                             |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | In der Regel verfügen Dialogfelder nicht über Tastenkombinationen. Wenn der Fenster Text für das Dialogfeld ein kaufmännisches und-Zeichen (&) enthält, gibt Microsoft Active Accessibility eine Zeichenfolge ungleich NULL als **KeyboardShortcut** -Eigenschaft zurück.                                                                                                                                                                                                                                        |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | Die **Name** -Eigenschaft ist der Fenster Text oder die Beschriftung, der in der Titelleiste des Dialog Felds angezeigt wird.                                                                                                                                                                                                                                                                                                                                                              |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | Bei der **Parent** -Eigenschaft handelt es sich um ein Fenster ( [**Rollen \_ System \_ Fenster**](object-roles.md) ), das das Dialogfeld umgibt und die **Name** -Eigenschaft und den Namen der Fenster Klasse wie das Dialogfeld enthält.                                                                                                                                                                                                                                                        |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | Die **Role** -Eigenschaft ist das [**\_ \_ Dialog Feld Rollensystem**](object-roles.md) oder das [**Rollen \_ System \_ PropertyPage**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): Zustands System nicht [**\_ \_**](object-state-constants.md) \| [**\_ \_ verfüg**](object-state-constants.md) bares Zustands System mit \| [**\_ \_ Fokus**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>Bemerkungen

Das Dialog Objekt bietet keine Unterstützung für die [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) -Methode. Um einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger auf ein Steuerelement in einem Dialogfeld zu erhalten, müssen Clients das Fenster Handle des Steuer Elements abrufen und dann [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

