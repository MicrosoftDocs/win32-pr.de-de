---
title: Der OBJID_QUERYCLASSNAMEIDX-Objektbezeichner
description: Microsoft Active Accessibility verwendet den OBJEKTbezeichner OBJID \_ QUERYCLASSNAMEIDX mit der WM GETOBJECT-Nachricht, um die Klasse zu bestimmen, zu der ein standardes Windows-Steuerelement oder ein allgemeines Steuerelement \_ gehört.
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d37ba879a6066ad07e1edda1aaa16551e8501906d187bac50d4a809179a8878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928966"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>Der OBJID \_ QUERYCLASSNAMEIDX-Objektbezeichner

Microsoft Active Accessibility verwendet den [**OBJEKTbezeichner OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) mit der [**WM \_ GETOBJECT-Nachricht,**](wm-getobject.md) um die Klasse zu bestimmen, zu der ein standardes Windows-Steuerelement oder ein allgemeines Steuerelement gehört. Ein Steuerelement antwortet auf diese Meldung, indem es einen Wert zurück gibt, Microsoft Active Accessibility dem Klassennamen des Steuerelements zu ordnet. Microsoft Active Accessibility verwendet diese Informationen, um Barrierefreiheitsunterstützung für Standardsteuerelemente Windows und allgemeine Steuerelemente zu bieten.

Im Allgemeinen antworten nur Windows Standardsteuerelemente und die allgemeinen Steuerelemente auf den [**OBJEKTbezeichner OBJID \_ QUERYCLASSNAMEIDX.**](object-identifiers.md) Ein benutzerdefiniertes Steuerelement kann jedoch auch antworten, wenn es die gleiche Funktionalität wie ein vorhandenes Standardsteuer Windows oder allgemeines Steuerelement enthält. Dadurch kann das benutzerdefinierte Steuerelement von einem der Standardproxyobjekte unterstützt werden, die von Microsoft Active Accessibility.

Weitere Informationen finden Sie unter [Anhang F: Objektbezeichnerwerte für OBJID \_ QUERYCLASSNAMEIDX](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md).

 

 




