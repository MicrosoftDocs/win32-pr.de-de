---
title: Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.
description: Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314823"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D bietet keine Unterstützung für das Rendern von Rich-Metadateien in Internet Explorer 9.

## <a name="platforms"></a>Plattformen

**Clients** – Windows Vista, Windows 7, Windows 8  
**Server** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012  




## <a name="description"></a>Beschreibung

Aufgrund interner Renderingänderungen in Internet Explorer 9 erstellen die [ihtmlelementrender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) -und [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) -APIs nun eine Metadatei mit einer einzelnen Bitmap, die den Webinhalt darstellt, anstelle einer umfangreichen Metadatei, die Text-und Vektor Informationen enthält. Diese Änderung wurde durch den Wechsel vom GDI-Rendering zu einem D2D-Rendering (Hardware-Accelerated Direct2D) verursacht.

Diese Änderung betrifft apps, die diese APIs verwenden und auf Text-oder Vektor Informationen in der Metadatei basieren.

## <a name="manifestation"></a>Ausstrahlung

Abhängig von der APP, die von dieser Änderung betroffen ist, sehen Benutzer möglicherweise ein fehlerhaftes oder falsches Verhalten in ihren apps.

## <a name="mitigation"></a>Minderung

Apps, die nur Textinformationen aus einem Webdokument (ohne Positionsinformationen) extrahieren müssen, können die [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) -Eigenschaft verwenden, um Text zu extrahieren.

Apps, die IViewObject::D RAW verwenden, können die [Funktion \_ iviewobjectdraw \_ DMLT9 mit dem \_ \_ GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) -Funktions Steuerungs Schlüssel verwenden, um das GDI-Rendering wiederherzustellen, wenn der Dokument Modus:

-   Ist kleiner oder gleich 8
-   Der FCK autorisiert diesen Host für die Verwendung von GDI.
-   Und ein metadateidc wird an die API übergeben.

## <a name="resources"></a>Ressourcen

-   [Ihtmlelementrender::D rawmondc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D RAW](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement:: InnerText-Eigenschaft](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Internet Funktions Steuerelemente (I... Int](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 