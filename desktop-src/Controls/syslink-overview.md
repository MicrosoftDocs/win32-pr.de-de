---
title: Informationen zu SysLink-Steuerelementen
description: Ein SysLink-Steuerelement ist ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf die eingebetteten Links klicken. Dieses Steuerelement stellt eine praktische Alternative zur Verwendung der Linkschaltfläche Befehl dar. Weitere Informationen finden Sie unter Schaltflächentypen.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4a5d64af48fc0b48b15f22fff55e5cb563339ac8d90446981c74e07f5d4713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168560"
---
# <a name="about-syslink-controls"></a>Informationen zu SysLink-Steuerelementen

Ein SysLink-Steuerelement ist ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf die eingebetteten Links klicken. Dieses Steuerelement stellt eine praktische Alternative zur Verwendung der [**Linkschaltfläche Befehl dar.**](button-styles.md) Weitere Informationen finden Sie unter [Schaltflächentypen](button-types-and-styles.md).

Jedes SysLink-Steuerelement kann mehrere Links unterstützen, und Sie können über einen nullbasierten Index auf jeden Link zugreifen. Das SysLink-Steuerelement ist in ComCtl32.dll Version 6 definiert und erfordert ein Manifest oder eine Direktive, die angibt, dass Version 6 der DLL verwendet werden soll, wenn sie verfügbar ist. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

Dieser Artikel enthält folgende Abschnitte.

-   [SysLink-Markup](#syslink-markup)
-   [Linkattribute](#link-attributes)
-   [Verknüpfungszustände](#link-states)
-   [Einschränkungen bei der bidirektionalen Textanzeige](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>SysLink-Markup

Das SysLink-Steuerelement unterstützt das Ankertag( a ) zusammen mit den &lt; &gt; **Attributen HREF** und **ID**. Ein **HREF kann** ein beliebiges Protokoll sein, z. B. http, ftp und mailto. Eine **ID** ist ein optionaler Name, der innerhalb eines SysLink-Steuerelements eindeutig ist und einem einzelnen Link zugeordnet ist. Links wird auch ein nullbasierter Index entsprechend ihrer Position innerhalb der Zeichenfolge zugewiesen. Dieser Index wird für den Zugriff auf einen Link verwendet.

## <a name="link-attributes"></a>Linkattribute

Die Attribute der einzelnen Links können entweder innerhalb des Ankertags für jeden Link oder durch Senden der [**LM \_ SETITEM-Nachricht festgelegt**](lm-setitem.md) werden. Wenn Sie ein Attribut festlegen, indem Sie es in der Initialisierungszeichenfolge angeben, wird lediglich der Wert initialisiert. Sie können den Wert eines Attributs durch nachfolgende Verwendung der **LM \_ SETITEM-Nachricht** ändern.

## <a name="link-states"></a>Verknüpfungszustände

Verknüpfungselemente können sich in einem von drei Zuzuständen wie den Flags in der folgenden Tabelle dargestellt haben.



| Statusflag   | Darstellung und Bedeutung                                            |
|--------------|-------------------------------------------------------------------|
| \_LIS-FOKUS | Der Link hat den Tastaturfokus, und durch Drücken der EINGABETASTE wird er aktiviert. |
| LIS \_ AKTIVIERT | Der Link ist aktiviert.                                              |
| LIS \_ VISITED | Der Benutzer hat die durch den Link dargestellte URL bereits besucht.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Einschränkungen bei der bidirektionalen Textanzeige

Einige Sprachen, z. B. Arabisch oder Hebräisch, werden von rechts nach links (RTL) geschrieben. Englisch wird von links nach rechts (LTR) geschrieben. Die Kombination von RTL und LTR wird als bidirektionaler Text bezeichnet. Das Mischen von LTR- und RTL Unicode- oder HTML-direktionalen Markupkonstrukten in Ressourcenzeichenfolgen als bidirektionale Flussmarker zum Steuern des Flusses von Zeichenfolgen führt bei Verwendung eines SysLink-Steuerelements möglicherweise nicht zum erwarteten Ergebnis. Beispielsweise wird ein MIT LTR markierter Satz möglicherweise nicht ordnungsgemäß im RTL-Kontext angezeigt.

> [!Note]  
> SysLink-Steuerelemente unterstützen keine bidirektionale Anzeige in allen Szenarien. Verwenden Sie ein SysLink-Steuerelement nur, wenn Sie wissen, dass ein einfaches LTR- oder RTL-Layout geeignet ist. Erwägen Sie andernfalls die Verwendung einer fortgeschritteneren Technologie wie [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).

 

 

 