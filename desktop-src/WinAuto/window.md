---
title: Window (MSAA UI-Elementreferenz)
description: Microsoft Active Accessibility erstellt ein generisches Fensterobjekt als Container für ein anderes Objekt. Cliententwickler übermitteln die Informationen von Fensterobjekten nicht an Endbenutzer, da diese Objekte keine nützlichen Informationen enthalten.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881eb863c6b12f8e72a9f48ba5ea290a2ad2f2471fa60683ee17e70c6271dad3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413270"
---
# <a name="window-msaa-ui-element-reference"></a>Window (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Window-Objekte** im Rahmen der MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Fensterobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Microsoft Active Accessibility erstellt ein generisches Fensterobjekt als Container für ein anderes Objekt. Cliententwickler übermitteln die Informationen von Fensterobjekten nicht an Endbenutzer, da diese Objekte keine nützlichen Informationen enthalten.

Wenn eine Serveranwendung ein benutzerdefiniertes Steuerelement erstellt, erstellt Microsoft Active Accessibility ein Fensterobjekt, das das benutzerdefinierte Steuerelement enthält. Der Server erstellt jedoch ein barrierefreies Objekt, um Informationen zum Inhalt des Steuerelements bereitzustellen. Das System generiert Ereignisse auf Objektebene für das Fensterobjekt, aber der Server muss Ereignisse für das barrierefreie Objekt senden, das Informationen über das Steuerelement bereitstellt.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Window-Objekt unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Fensterobjekt unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft die [IDispatch-Schnittstelle](idispatch-interface.md) des angegebenen untergeordneten -Element ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **ChildCount-Eigenschaft** ist 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Das Fensterobjekt selbst verfügt nicht über eine **Description-Eigenschaft.** Die **Description-Eigenschaft** für das untergeordnete Objekt kann über das Fensterobjekt abgerufen werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Das Fensterobjekt selbst verfügt nicht über eine **KeyboardShortcut-Eigenschaft.** Die **KeyboardShortcut-Eigenschaft** für das untergeordnete Objekt wird über das Fensterobjekt abgerufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name-Eigenschaft** des Fensterobjekts ist identisch mit dem untergeordneten Objekt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role-Eigenschaft** ist [**ROLE SYSTEM \_ \_ WINDOW.**](object-roles.md) Die **Rolle** des untergeordneten Objekts wird über das Fensterobjekt abgerufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State-Eigenschaft** ist eine Kombination aus einem oder mehreren der folgenden [Werte:](object-state-constants.md) [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ UNAVAILABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ SIZEABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ MOVEABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notizen

Die Ereignisse [**EVENT \_ SYSTEM \_ DRAGDROPSTART,**](event-constants.md) [**EVENT SYSTEM \_ \_ DRAGDROPEND,**](event-constants.md) [**EVENT OBJECT \_ \_ HIDE**](event-constants.md)und [**EVENT OBJECT \_ \_ PARENTCHANGE**](event-constants.md) werden nicht vom Fensterobjekt gesendet. Dies ist ein bekanntes Problem, das behoben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





