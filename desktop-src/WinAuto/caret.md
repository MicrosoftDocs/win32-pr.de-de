---
title: Caretzeichen (MSAA-Benutzeroberflächen Element-Referenz)
description: Die Einfügemarke ist eine blinkende Linie, ein Block oder eine Bitmap im Client Bereich eines Fensters oder in einem Steuerelement, das Tastatureingaben annimmt.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103857944"
---
# <a name="caret-msaa-ui-element-reference"></a>Caretzeichen (MSAA-Benutzeroberflächen Element-Referenz)

> [!Note]  
> In diesem Thema werden die Einfügevorgänge für die MSAA-Benutzeroberflächen Element Referenz beschrieben. Die Verwendung von Caretzeichen in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Die Einfügemarke ist eine blinkende Linie, ein Block oder eine Bitmap im Client Bereich eines Fensters oder in einem Steuerelement, das Tastatureingaben annimmt. Gibt den Ort an, an dem Text oder Grafiken eingefügt werden. Da jeweils nur ein Fenster den Tastaturfokus besitzt, gibt es nur eine Einfügemarke im System.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Der Caretzeichen unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Die Einfügemarke unterstützt die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>Kommentare</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>Die <strong>childCount</strong> -Eigenschaft ist 0 (null).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></td>
<td>Die <strong>Name</strong> -Eigenschaft ist " &quot; Edit" &quot; .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></td>
<td>Die <strong>Role</strong> -Eigenschaft ist <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></td>
<td>Mögliche Werte für die <strong>State</strong> -Eigenschaft sind:
<ul>
<li>NULL, was bedeutet, dass die Einfügemarke sichtbar ist</li>
<li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Notizen

-   Anders als andere Elemente der Benutzeroberfläche verfügt das Caretzeichen über kein zugeordnetes Fenster handle. Um Zugriff auf das Caretzeichen-Objekt zu erhalten, müssen Clients ein [*wineventproc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) festlegen und auf das Generieren von Ereignissen durch das Caretzeichen warten.
-   Das Caretzeichen-Objekt im Rich Edit-Steuerelement, das von Riched20.dll bereitgestellt wird (das in Text-Editoren wie Microsoft WordPad in Windows 98 verwendet wird), sendet keine [WinEvents](winevents-infrastructure.md) , wenn seine Position während der Textauswahl geändert wird. Wenn Benutzer die UMSCHALTTASTE und die Pfeiltasten drücken, um Text auszuwählen, löst das Caretzeichen Objekt das [**Ereignis \_ Objekt \_ locationchange**](event-constants.md) WinEvent nicht aus. Wenn die Auswahlprogramm gesteuert durch Rich-Edit-Meldungen festgelegt wird, sendet das Caretzeichen-Objekt auch keine Ereignisse, um die neue Position anzugeben.

    Alle Anwendungen, die Riched20.dll verwenden, weisen dieses Problem auf. Anwendungen, die frühere Versionen des Rich Edit-Steuer Elements verwenden, senden Ereignisse auf der Grundlage der Auswahl ordnungsgemäß.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




