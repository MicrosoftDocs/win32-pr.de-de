---
description: Sie können eine benutzerdefinierte Gestenerkennung unabhängig voneinander oder zusätzlich zu GestureRecognizer verwenden. Erstellen Sie Ihre benutzerdefinierte Gestenerkennung als IStylusSyncPlugin, lassen Sie sie CustomStylusData erstellen, und fügen Sie das Plug-In in die gleiche StylusSyncPluginCollection wie GestureRecognizer ein. Kombinieren Sie in IStylusSyncPlugin Gestenbenachrichtigungen von beiden Erkennungen in Benachrichtigungen, die von einer Anwendung genutzt werden.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Verwenden einer benutzerdefinierten Gestenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4c58dd93bdb19f1f930be38e40f0068fa02239f09603035b572559d1f8a916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091304"
---
# <a name="using-a-custom-gesture-recognizer"></a>Verwenden einer benutzerdefinierten Gestenerkennung

Sie können eine benutzerdefinierte Gestenerkennung unabhängig oder zusätzlich zum [**GestureRecognizer**](gesturerecognizer-class.md)verwenden.

Erstellen Sie Ihre benutzerdefinierte Gestenerkennung als [**IStylusSyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)lassen Sie [sie CustomStylusData](/previous-versions/ms575208(v=vs.100))erstellen, und schließen Sie das Plug-In in die gleiche [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) wie [**die GestureRecognizer-Datei**](gesturerecognizer-class.md)ein. Kombinieren Sie in **IStylusSyncPlugin** Gestenbenachrichtigungen von beiden Erkennungen in Benachrichtigungen, die von einer Anwendung genutzt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf und Bearbeiten von Stifteingaben](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
