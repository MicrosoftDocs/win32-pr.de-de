---
title: Caret (MSAA UI-Elementreferenz)
description: Das Caretelement ist eine blinkende Linie, ein Block oder eine Bitmap im Clientbereich eines Fensters oder in einem Steuerelement, das Tastatureingaben akzeptiert.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467297"
---
# <a name="caret-msaa-ui-element-reference"></a>Caret (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden Carets für die MsAA UI-Elementreferenz beschrieben. Die Verwendung von Carets in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Das Caretelement ist eine blinkende Linie, ein Block oder eine Bitmap im Clientbereich eines Fensters oder in einem Steuerelement, das Tastatureingaben akzeptiert. Sie gibt die Stelle an, an der Text oder Grafiken eingefügt werden. Da nur jeweils ein Fenster den Tastaturfokus besitzt, gibt es nur einen Caretpunkt im System.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Das Caret-Tag unterstützt die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Das Caretobjekt unterstützt die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)




| Eigenschaft | Kommentare | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | Die <strong>ChildCount-Eigenschaft</strong> ist 0 (null). | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | Die <strong>Name-Eigenschaft</strong> ist "Bearbeiten". | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | Die <strong>Role-Eigenschaft</strong> ist <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | Mögliche Werte für die <strong>State-Eigenschaft:</strong><ul><li>0 (null), was bedeutet, dass der Caretpunkt sichtbar ist.</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>Hinweise

-   Im Gegensatz zu anderen Benutzeroberflächenelementen verfügt das Caretobjekt nicht über ein zugeordnetes Fensterhandle. Um Zugriff auf das Caretobjekt zu erhalten, müssen Clients [*winEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) festlegen und warten, bis das Caretobjekt Ereignisse generiert.
-   Das Caretzeichenobjekt im Rich Edit-Steuerelement, das von Riched20.dll bereitgestellt wird (das in Text-Editoren wie Microsoft WordPad in Windows 98 verwendet wird) sendet keine [WinEvents,](winevents-infrastructure.md) wenn seine Position während der Textauswahl geändert wird. Wenn Benutzer die UMSCHALTTASTE und die Pfeiltasten drücken, um Text auszuwählen, löst das Caretobjekt das [**EVENT \_ OBJECT \_ LOCATIONCHANGE**](event-constants.md) WinEvent nicht aus. Ebenso sendet das Caretobjekt keine Ereignisse, um seine neue Position anzugeben, wenn die Auswahl programmgesteuert durch Rich-Edit-Nachrichten festgelegt wird.

    Alle Anwendungen, die Riched20.dll verwenden, weisen dieses Problem auf. Anwendungen, die frühere Versionen des Rich Edit-Steuerelements verwenden, senden Ereignisse basierend auf der Auswahl ordnungsgemäß.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




