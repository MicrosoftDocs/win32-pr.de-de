---
title: Titelleiste (MSAA UI-Element Referenz)
description: Die Titelleiste am oberen Rand eines Fensters zeigt ein Anwendungs definiertes Symbol und eine Textzeile an.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104389788"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Titelleiste (MSAA UI-Element Referenz)

> [!Note]  
> In diesem Thema werden **Titel** leisten Objekte für den MSAA-Benutzeroberflächen-Element Verweis beschrieben. Das Erstellen von **Titel** leisten Objekten in verschiedenen Benutzeroberflächen-Frameworks wird hier nicht beschrieben. Weitere Informationen finden Sie in der API-Referenz Dokumentation für das von Ihnen verwendete UI-Framework.

 

Die Titelleiste am oberen Rand eines Fensters zeigt ein Anwendungs definiertes Symbol und eine Textzeile an. Der Text gibt den Namen der Anwendung an und gibt den Zweck des Fensters an. Die Titelleiste ermöglicht es dem Benutzer auch, das Fenster mit einer Maus oder einem anderen Zeigegerät zu verschieben.

Titelleisten enthalten mindestens drei kleine Schaltflächen zum minimieren, maximieren oder wiederherstellen und zum Schließen des Fensters, das mit der Titelleiste verknüpft ist. Titelleisten enthalten außerdem eine kontextabhängige Hilfe Schaltfläche. Anwendungen, die in der Far-East Version des Windows-Betriebssystems ausgeführt werden, können auch Schaltflächen für Eingabemethoden-Editor (IME) enthalten. Microsoft Active Accessibility macht diese Schaltflächen als untergeordnete Elemente der Titelleiste verfügbar.

## <a name="iaccessible-methods"></a>IAccessible-Methoden

Titelleisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Methoden:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>IAccessible-Eigenschaften

Titelleisten unterstützen die folgenden [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Eigenschaften:



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
<td>Die <strong>childCount</strong> -Eigenschaft ist 5. Die <strong>childCount</strong> -Eigenschaft enthält die Schaltflächen IME und kontextabhängige Hilfe, auch wenn Sie nicht angezeigt werden. Schaltflächen, die nicht angezeigt werden, haben die Eigenschaft <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>Die <strong>Description</strong> -Eigenschaft der Titelleiste selbst ist: &quot; zeigt den Namen des Fensters an und enthält Steuerelemente zum Bearbeiten. &quot; Die untergeordneten Schaltflächen in der Titelleiste haben folgende Beschreibungen:<br/>
<ul>
<li>&quot;Verschiebt das Fenster aus</li>
<li>&quot;Macht das Fenster voll</li>
<li>&quot;Legt eine minimierte oder</li>
<li>&quot;Schließt das Fenster.&quot;</li>
<li>&quot;Gibt einen Kontext ein oder verlässt ihn:</li>
<li>&quot;Zeigt die Tastatur beim Drücken an&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>Die <strong>Name</strong> -Eigenschaft wird von der Titelleiste selbst nicht unterstützt. Die untergeordneten Schaltflächen in der Titelleiste haben die folgenden Namen:
<ul>
<li>&quot;Minimieren&quot;</li>
<li>&quot;Maximieren &quot; oder &quot; Wiederherstellen &quot; ,</li>
<li>&quot;Close&quot;</li>
<li>&quot;Kontexthilfe&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>Die <strong>Parent</strong> -Eigenschaft der Titelleiste ist das Hauptanwendungsfenster ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ), das denselben Anwendungs definierten Fenster Klassennamen wie die Titelleiste hat.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>Die <strong>Role</strong> -Eigenschaft ist <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. In den untergeordneten Schaltflächen in der Titelleiste ist die <strong>Role</strong> -Eigenschaft <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>Die <strong>State</strong> -Eigenschaft für die Titelleiste und die untergeordneten Schaltflächen können eine Kombination aus einem oder mehreren der folgenden <a href="object-state-constants.md">Werte</a>sein: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>Die <strong>value</strong> -Eigenschaft ist eine Zeichenfolge, die dem in der Titelleiste angezeigten Text entspricht.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Notizen

-   Obwohl die Titelleiste einer Anwendung **das State-** eigenschaftflag **für das Zustands** System als [**\_ \_ focverwendbare**](object-state-constants.md)Eigenschaft aufweist, hat Sie niemals das Statusflag [**State \_ System \_ fokussiert**](object-state-constants.md). Beim Festlegen des Fokus auf ein Titelleisten Objekt wird das Anwendungsfenster fokussiert.
-   Da das Titelleisten Objekt [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)nicht unterstützt, sind die Schaltflächen auf der Titelleiste einfache Elemente. Die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle selbst wird nicht unterstützt. Das Titelleisten Objekt enthält Informationen zu diesen untergeordneten Schaltflächen.
-   Da Titelleisten keinen Fokus erhalten und keine Standardaktion haben, werden die Methoden [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) und [**get \_ accdefaultaction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) für dieses Steuerelement nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IAccessible-Schnittstelle](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





