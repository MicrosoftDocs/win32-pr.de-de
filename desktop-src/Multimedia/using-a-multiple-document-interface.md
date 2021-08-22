---
title: Verwenden einer Schnittstelle für mehrere Dokumente
description: Verwenden einer Schnittstelle für mehrere Dokumente
ms.assetid: bc59f19c-1064-4df8-8864-38e6d188f92f
keywords:
- MCIWndRegisterClass-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b75d337c5375b66974161c1c983c1aeec5bed7805457186139771d879132b6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941055"
---
# <a name="using-a-multiple-document-interface"></a>Verwenden einer Schnittstelle für mehrere Dokumente

Anwendungen, die eine MDI (Multiple Document Interface) verwenden, müssen möglicherweise Fensterstile angeben, die nicht über die [**MCIWndCreate-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) verfügbar sind. Für diese Anwendungen können Sie ein MCIWnd-Fenster registrieren und erstellen, indem Sie die [**MCIWndRegisterClass-Funktion**](/windows/desktop/api/Vfw/nf-vfw-mciwndregisterclass) mit der [CreateWindowEx-Funktion](/windows/win32/api/winuser/nf-winuser-createwindowexa) verwenden. Die **MCIWndRegisterClass-Funktion** registriert die Fensterklasse MCIWND \_ WINDOW CLASS und erstellt dann \_ **createWindowEx** eine Instanz eines MCIWnd-Fensters.

 

 