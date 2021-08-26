---
title: Direct2D unterstützt das Rendern in rich metafiles in Internet Explorer 9 nicht.
description: Direct2D unterstützt das Rendern in rich metafiles in Internet Explorer 9 nicht.
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebe10310202385fa4e9458cb1a442cbf98a3f6f178331d888c096449631ca61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057350"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D unterstützt das Rendern in rich metafiles in Internet Explorer 9 nicht.

## <a name="platforms"></a>Plattformen

**Clients** – Windows Vista, Windows 7, Windows 8  
**Server** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012  




## <a name="description"></a>BESCHREIBUNG

Aufgrund interner Renderingänderungen in Internet Explorer 9 erstellen die [IHTMLElementRender::D rawToDC-](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) und [IViewObject::D raw-APIs](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) jetzt eine Metadatei, die eine einzelne Bitmap enthält, die den Webinhalt darstellt, anstatt eine umfangreiche Metadatei mit Text- und Vektorinformationen. Diese Änderung wurde durch den Wechsel vom GDI-Rendering zum hardwarebeschleunigten Direct2D-Rendering (D2D) bedingt.

Diese Änderung betrifft Apps, die diese APIs verwenden und Text- oder Vektorinformationen in der Metadatei verwenden.

## <a name="manifestation"></a>Manifestation

Abhängig von der App, die von dieser Änderung betroffen ist, können Benutzer fehlerhaftes oder falsches Verhalten in ihren Apps sehen.

## <a name="mitigation"></a>Minderung

Apps, die nur Textinformationen aus einem Webdokument extrahieren müssen (ohne Positionierungsinformationen), können die [innerText-Eigenschaft](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) verwenden, um Text zu extrahieren.

Apps, die IViewObject::D raw verwenden, können den [ \_ FEATURE-IVIEWOBJECTDRAW \_ DMLT9 \_ WITH \_ GDI-Featuresteuerschlüssel](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) verwenden, um im Dokumentmodus zum GDI-Rendering zurück zu wechseln:

-   Ist kleiner oder gleich 8
-   Der FCK autorisiert diesen Host zur Verwendung von GDI.
-   Ein Metadatei-DC wird an die API übergeben.

## <a name="resources"></a>Ressourcen

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D raw](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [IHTMLElement::innerText-Eigenschaft](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Steuerelemente für Internetfeatures (d. h. L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 