---
title: Fenster (MSAA-Benutzeroberflächen-Element Referenz)
description: Microsoft Active Accessibility erstellt ein generisches Fenster Objekt als Container für ein anderes Objekt. Client Entwickler übermitteln die Informationen von Window-Objekten nicht an Endbenutzer, da diese Objekte keine nützlichen Informationen enthalten.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709270"
---
# <a name="window-msaa-ui-element-reference"></a>Fenster (MSAA-Benutzeroberflächen-Element Referenz)

> [!Note]  
> In diesem Thema werden **Fenster** Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Die Vorgehensweise zum Erstellen von **Fenster** Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Microsoft Active Accessibility erstellt ein generisches Fenster Objekt als Container für ein anderes Objekt. Client Entwickler übermitteln die Informationen von Window-Objekten nicht an Endbenutzer, da diese Objekte keine nützlichen Informationen enthalten.

Wenn eine Serveranwendung ein benutzerdefiniertes Steuerelement erstellt, erstellt Microsoft Active Accessibility ein Fenster Objekt, das das benutzerdefinierte Steuerelement enthält. der Server erstellt jedoch ein Barrierefreies Objekt, das Informationen über den Inhalt des Steuer Elements bereitstellt. Das System generiert Ereignisse auf Objektebene für das Window-Objekt, aber der Server muss Ereignisse für das barrierefreie Objekt senden, das Informationen über das Steuerelement bereitstellt.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Window-Objekt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Window-Objekt unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



| Eigenschaft                                                                             | Kommentare                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_accChild erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Ruft die [IDispatch](idispatch-interface.md) -Schnittstelle des angegebenen untergeordneten-Elements ab.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | Die **childCount** -Eigenschaft ist 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get- \_ accdescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Das Fenster Objekt selbst weist keine **Beschreibungs** Eigenschaft auf. Die **Description** -Eigenschaft für das untergeordnete Objekt kann über das Window-Objekt abgerufen werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_Zugriffs Fokus erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_accKeyboardShortcut erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Das Fenster Objekt selbst hat keine **KeyboardShortcut** -Eigenschaft. Die **KeyboardShortcut** -Eigenschaft für das untergeordnete Objekt wird über das Window-Objekt abgerufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**\_accName erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Die **Name** -Eigenschaft des Window-Objekts ist mit dem untergeordneten Objekt identisch.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_accParent erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**get- \_ Zugriffs Rolle**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | Die **Role** -Eigenschaft ist das [**\_ \_ Fenster "Rollen System**](object-roles.md)". Die **Rolle** des untergeordneten Objekts wird über das Window-Objekt abgerufen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**\_accState erhalten**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Die **State** -Eigenschaft ist eine Kombination aus einem oder mehreren der folgenden [Werte](object-state-constants.md): [**Zustands System \_ \_ unsichtbar**](object-state-constants.md) Zustands System nicht verfügbar Zustands System verfügbar Zustands Systemzustands System mit \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**Fokus \_ \_**](object-state-constants.md) \| [**\_ \_ nutzbarem**](object-state-constants.md) Zustands \| [**\_ \_**](object-state-constants.md) System mit Fokus<br/> |



 

## <a name="notes"></a>Notizen

Das [**Ereignis Ereignis \_ System \_ dragdropstart**](event-constants.md), [**Ereignis \_ System \_ dragdropend**](event-constants.md), [**Ereignis \_ Objekt \_ Ausblenden**](event-constants.md)und [**\_ ereignisobjektobjektänderung \_**](event-constants.md) werden nicht vom Fenster Objekt gesendet. Dies ist ein bekanntes Problem und wird behandelt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





