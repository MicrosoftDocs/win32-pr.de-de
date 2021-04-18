---
title: Der OBJID_QUERYCLASSNAMEIDX Objekt Bezeichner.
description: Microsoft Active Accessibility verwendet die objID \_ queryclassnameidx-Objekt-ID mit der WM \_ GetObject-Nachricht, um die Klasse zu bestimmen, zu der ein standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement gehört.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337347"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>Der ObjID \_ queryclassnameidx-Objekt Bezeichner

Microsoft Active Accessibility verwendet die [**objID \_ queryclassnameidx**](object-identifiers.md) -Objekt-ID mit der [**WM \_ GetObject**](wm-getobject.md) -Nachricht, um die Klasse zu bestimmen, zu der ein standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement gehört. Ein-Steuerelement reagiert auf diese Meldung, indem ein Wert zurückgegeben wird, den Microsoft Active Accessibility dem Klassennamen des Steuer Elements zuordnet. Microsoft Active Accessibility verwendet diese Informationen, um Barrierefreiheits Unterstützung für standardmäßige Windows-Steuerelemente und allgemeine Steuerelemente bereitzustellen.

Im allgemeinen reagieren nur die standardmäßigen Windows-Steuerelemente und die allgemeinen Steuerelemente auf die [**objID \_ queryclassnameidx**](object-identifiers.md) -Objekt Kennung. Ein benutzerdefiniertes Steuerelement kann jedoch auch Antworten, wenn es die gleiche Funktionalität wie ein vorhandenes standardmäßiges Windows-Steuerelement oder ein gemeinsames Steuerelement enthält. Dadurch wird das benutzerdefinierte Steuerelement von einem der Standard Proxy Objekte, die von Microsoft Active Accessibility bereitgestellt werden, unterstützt.

Weitere Informationen finden Sie unter [Anhang F: objektbezeichnerwerte für objID \_ queryclassnameidx](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 




