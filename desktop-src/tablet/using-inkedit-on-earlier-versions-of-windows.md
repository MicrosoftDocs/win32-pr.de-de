---
description: Aufgrund des Mangels an Erkennungen in Nicht-Tablet-PC-Editionen von Microsoft Windows XP können Sie InkEdit nicht zum Rendern von Ink auf Windows 2000, Windows Server 2003 und Nicht-Tablet-PC-Editionen von Windows XP verwenden, und Sie können das Steuerelement nicht zum Eingeben von Ink auf diesen Betriebssystemen verwenden.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Verwenden von InkEdit in früheren Versionen von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966609"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Verwenden von InkEdit in früheren Versionen von Windows

Aufgrund des Mangels an Erkennungen in Nicht-Tablet PC-Editionen von Microsoft Windows XP können Sie [InkEdit](inkedit-control.md) nicht zum Rendern von Ink auf Windows 2000, Windows Server 2003 und Nicht-Tablet PC Editionen von Windows XP verwenden, und Sie können das Steuerelement nicht verwenden, um Ink auf diesen Betriebssystemen einzugeben.

Die [**InkMode-Eigenschaft**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) des Steuerelements ist auf **Disabled** **(IEM \_ Disabled** for C++) festgelegt, und der Versuch, die Eigenschaft zu ändern, hat keine Auswirkungen. Sie können anderen Eigenschaften Werte zuweisen und Ink in andere Anwendungen kopieren und einfügen, aber Sie können das -Steuerelement nicht verwenden, um Gesten zu akzeptieren oder Ink zu sammeln.

 

 



