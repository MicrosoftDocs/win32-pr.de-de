---
title: Titelleiste (MSAA UI-Elementreferenz)
description: Die Titelleiste am oberen Rand eines Fensters zeigt ein anwendungsdefiniertes Symbol und eine Textzeile an.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9183e4c4f5364fb45ba2a73dd2d40509c03c7838bbb248e1d95765b675f50cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994000"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Titelleiste (MSAA UI-Elementreferenz)

> [!Note]  
> In diesem Thema werden **Titelleistenobjekte** für die MSAA UI-Elementreferenz beschrieben. Das Erstellen von **Titelleistenobjekten** in verschiedenen Benutzeroberflächenframeworks wird hier nicht beschrieben. Informationen zum verwendeten BENUTZERoberflächenframework finden Sie in der API-Referenzdokumentation.

 

Die Titelleiste am oberen Rand eines Fensters zeigt ein anwendungsdefiniertes Symbol und eine Textzeile an. Der Text gibt den Namen der Anwendung und den Zweck des Fensters an. Die Titelleiste ermöglicht dem Benutzer auch das Verschieben des Fensters mit der Maus oder einem anderen zeigenden Gerät.

Titelleisten enthalten mindestens drei kleine Schaltflächen, die das der Titelleiste zugeordnete Fenster minimieren, maximieren oder wiederherstellen und schließen. Titelleisten enthalten auch eine kontextbezogene Hilfeschaltfläche. Anwendungen, die in der Far-East Version des Windows Betriebssystems ausgeführt werden, können auch IME-Schaltflächen (Input Method Editor) enthalten. Microsoft Active Accessibility macht diese Schaltflächen als untergeordnete Elemente der Titelleiste verfügbar.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Titelleisten unterstützen die folgenden [**IAccessible-Methoden:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Titelleisten unterstützen die folgenden [**IAccessible-Eigenschaften:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



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
<td>Die <strong>ChildCount-Eigenschaft</strong> ist fünf. Die <strong>ChildCount-Eigenschaft</strong> enthält die IME- und kontextabhängigen Hilfeschaltflächen, auch wenn sie nicht angezeigt werden. Schaltflächen, die nicht angezeigt werden, verfügen über die <strong>State-Eigenschaft</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>Die <strong>Description-Eigenschaft</strong> der Titelleiste selbst lautet: &quot; Zeigt den Namen des Fensters an und enthält Steuerelemente, um es zu bearbeiten. &quot; Die untergeordneten Schaltflächen in der Titelleiste weisen die folgenden Beschreibungen auf:<br/>
<ul>
<li>&quot;Verschiebt das Fenster aus</li>
<li>&quot;Macht das Fenster voll</li>
<li>&quot;Legt eine minimierte oder</li>
<li>&quot;Schließt das Fenster.&quot;</li>
<li>&quot;Eintritt in oder Verlassen des Kontexts:</li>
<li>&quot;Ruft die Tastatur auf, wenn sie gedrückt wird&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>Die Titelleiste selbst unterstützt die <strong>Name-Eigenschaft</strong> nicht. Die untergeordneten Schaltflächen in der Titelleiste haben die folgenden Namen:
<ul>
<li>&quot;Minimieren&quot;</li>
<li>&quot;Maximieren &quot; oder &quot; Wiederherstellen &quot; von</li>
<li>&quot;Close&quot;</li>
<li>&quot;Kontexthilfe&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>Die <strong>Parent-Eigenschaft</strong> der Titelleiste ist das Hauptanwendungsfenster ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ), das den gleichen anwendungsdefinierte Fensterklassennamen wie die Titelleiste auf hat.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>Die <strong>Role-Eigenschaft</strong> ist <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Die untergeordneten Schaltflächen in der Titelleiste verfügen über die <strong>Role-Eigenschaft</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>Die <strong>State-Eigenschaft</strong> für die Titelleiste und die untergeordneten Schaltflächen kann eine Kombination aus einem oder mehreren der folgenden <a href="object-state-constants.md">Werte</a>sein: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>Die <strong>Value-Eigenschaft</strong> ist eine Zeichenfolge, die mit dem in der Titelleiste angezeigten Text identisch ist.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Hinweise

-   Obwohl die Titelleiste einer Anwendung über das **State-Eigenschaftenflag** [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)verfügt, weist sie nie das **State-Flag** STATE [**SYSTEM \_ \_ FOCUSED**](object-state-constants.md)auf. Das Festlegen des Fokus auf ein Titelleistenobjekt konzentriert das Anwendungsfenster.
-   Da das Titelleistenobjekt [**"get \_ accChild"**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)nicht unterstützt, sind die Schaltflächen auf der Titelleiste einfache Elemente. Sie unterstützen die [**IAccessible-Schnittstelle**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) selbst nicht. Das Titelleistenobjekt enthält Informationen zu diesen untergeordneten Schaltflächen.
-   Da Titelleisten keinen Fokus erhalten und keine Standardaktion aufweisen, werden die [**accDoDefaultAction-**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) und [**\_ get accDefaultAction-Methoden**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) für dieses Steuerelement nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





