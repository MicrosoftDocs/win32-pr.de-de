---
description: Verarbeiten von Unicode in einer IME-Aware Anwendung
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Verarbeiten von Unicode in einer IME-Aware Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349717"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Verarbeiten von Unicode in einer IME-Aware Anwendung

Mit dem imm und der Handhabung von Unicode sind zwei Probleme verbunden. Das erste Problem besteht darin, dass die Unicode-Versionen der imm-Funktionen die Größe eines Puffers in Bytes anstelle von 16-Bit-Unicode-Zeichen abrufen. Das zweite Problem besteht darin, dass der imm normalerweise Unicode-Zeichen (anstelle von DBCS-Zeichen) in den Zeichen Nachrichten [**WM \_ char**](../inputdev/wm-char.md) und [**WM \_ IME \_**](wm-ime-char.md) abruft.

Windows unterstützt eine Unicode-Schnittstelle für das IMM, zusätzlich zur ursprünglich unterstützten ANSI-Schnittstelle.

Ihre Anwendungen sollten [**registerclassw**](/windows/win32/api/winuser/nf-winuser-registerclassa) verwenden, damit die " [**WM \_ char**](../inputdev/wm-char.md) "-und " [**WM IME"- \_ \_ char**](wm-ime-char.md) -Nachrichten anstelle von DBCS-Zeichen im *wParam* -Parameter Unicode-Zeichen abrufen können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Eingabemethoden-Managers](using-input-method-manager.md)
</dt> </dl>

 

 
