---
title: Informationen über Syslink-Steuerelemente
description: Bei einem Syslink-Steuerelement handelt es sich um ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf Ihre eingebetteten Hyperlinks klicken. Dieses Steuerelement stellt eine bequeme Alternative zum Verwenden der Befehls Link Schaltfläche dar. Weitere Informationen finden Sie unter Schaltflächen Typen.
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039671"
---
# <a name="about-syslink-controls"></a>Informationen über Syslink-Steuerelemente

Bei einem Syslink-Steuerelement handelt es sich um ein Fenster, das markierten Text rendert und die Anwendung benachrichtigt, wenn Benutzer auf Ihre eingebetteten Hyperlinks klicken. Dieses Steuerelement stellt eine bequeme Alternative zum Verwenden der [**Befehls Link Schaltfläche**](button-styles.md)dar. Weitere Informationen finden Sie unter [Schaltflächen Typen](button-types-and-styles.md).

Jedes Syslink-Steuerelement kann mehrere Hyperlinks unterstützen, und Sie können auf jeden Link über einen NULL basierten Index zugreifen. Das Syslink-Steuerelement wird in der ComCtl32.dll Version 6 definiert und erfordert ein Manifest oder eine Direktive, die angibt, dass Version 6 der dll verwendet werden soll, wenn Sie verfügbar ist. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

Dieser Artikel enthält folgende Abschnitte.

-   [Syslink-Markup](#syslink-markup)
-   [Verknüpfungs Attribute](#link-attributes)
-   [Link Zustände](#link-states)
-   [Einschränkungen bei der bidirektionalen Text Anzeige](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a>Syslink-Markup

Das Syslink-Steuerelement unterstützt das Anchor-Tag ( &lt; a &gt; ) zusammen mit den Attributen **href** und **ID**. Ein **href** kann ein beliebiges Protokoll sein, z. b. http, FTP und mailto. Eine **ID** ist ein optionaler Name, der innerhalb eines Syslink-Steuer Elements eindeutig ist und mit einem einzelnen Link verknüpft ist. Links wird auch ein NULL basierter Index gemäß ihrer Position innerhalb der Zeichenfolge zugewiesen. Dieser Index wird für den Zugriff auf einen Link verwendet.

## <a name="link-attributes"></a>Verknüpfungs Attribute

Die Attribute jedes Links können entweder innerhalb des Anker Tags für die einzelnen Links oder durch Senden der [**LM- \_ SetItem**](lm-setitem.md) -Nachricht festgelegt werden. Durch Festlegen eines Attributs durch Angabe in der Initialisierungs Zeichenfolge wird der Wert lediglich initialisiert. Sie können den Wert eines Attributs durch nachfolgende Verwendung der **LM- \_** Nachricht nach dem Festlegen der Nachricht ändern.

## <a name="link-states"></a>Link Zustände

Verknüpfungs Elemente können einen von drei Zuständen aufweisen, die durch die-Flags in der folgenden Tabelle dargestellt werden.



| Statusflag   | Darstellung und Bedeutung                                            |
|--------------|-------------------------------------------------------------------|
| LIS im \_ Fokus | Der Link hat den Tastaturfokus, und durch Drücken der EINGABETASTE wird er aktiviert. |
| LIS \_ aktiviert | Der Link ist aktiviert.                                              |
| LIS \_ besucht | Der Benutzer hat die durch den Link dargestellte URL bereits besucht.     |



 

## <a name="limitations-on-bidirectional-text-display"></a>Einschränkungen bei der bidirektionalen Text Anzeige

Einige Sprachen, z. b. Arabisch oder Hebräisch, werden von rechts nach links (RTL) geschrieben. Englisch wird von links nach rechts (LTR) geschrieben. Das Kombinieren von RTL mit Ltr heißt bidirektionaler Text. Wenn Sie in Ressourcen Zeichenfolgen als bidirektionale Fluss Marker, die den Ablauf von Zeichen folgen steuern, eine Kombination aus LTR-und RTL-Unicode-oder HTML-direktionalen Markup-Konstrukten durchführen Beispielsweise kann ein mit Ltr markierten Satz im RTL-Kontext nicht ordnungsgemäß angezeigt werden.

> [!Note]  
> Syslink-Steuerelemente unterstützen nicht die bidirektionale Anzeige in allen Szenarien. Verwenden Sie ein Syslink-Steuerelement nur, wenn Sie wissen, dass ein einfaches ltr-oder RTL-Layout ausreichend ist. Andernfalls sollten Sie die Verwendung einer erweiterten Technologie wie [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))in Erwägung gezogen.

 

 

 