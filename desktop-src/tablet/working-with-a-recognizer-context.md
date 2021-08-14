---
description: Das Divider-Objekt verwendet einen RecognizerContext, um die Analyse von Erkennungssegmenten zu verbessern und Erkennungstext für Handschriftelemente zu generieren.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Arbeiten mit einem Erkennungskontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d99020e97170f0b68b1459abdc4b85f81ebc3fbba426233c2c13b5e042f28ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715098"
---
# <a name="working-with-a-recognizer-context"></a>Arbeiten mit einem Erkennungskontext

Das [**Divider-Objekt**](inkdivider-class.md) verwendet einen [**RecognizerContext,**](inkrecognizercontext-class.md) um die Analyse von Erkennungssegmenten zu verbessern und Erkennungstext für Handschriftelemente zu generieren.

Sie können den Erkennungskontext festlegen, indem Sie die [**RecognizerContext-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) des [**Divider-Objekts**](inkdivider-class.md) verwenden oder den Erkennungskontext im Aufruf des [Divider-Konstruktors](/previous-versions/ms839465(v=msdn.10)) (in verwaltetem Code) bereitstellen. Wenn der **RecognizerContext-Eigenschaft** ein Erkennungskontext für eine nicht handschriftliche Erkennung oder für eine Erkennung zugewiesen wird, die die freie Eingabefunktion nicht unterstützt, wird eine Ausnahme ausgelöst.

Wenn keine Erkennungen installiert sind oder dem [**Divider-Objekt**](inkdivider-class.md) kein Erkennungskontext zugewiesen ist, verwendet das **Divider-Objekt** keinen Erkennungskontext. In diesem Fall führt die Layoutanalysefunktion die Segmentteilung durch, und dem [**DivisionResult-Objekt**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) ist kein Text zugeordnet.

> [!Note]  
> Die [**RecognizerContext-Eigenschaft**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) kann nicht mehr geändert werden, nachdem dem [**Divider-Objekt**](inkdivider-class.md) Striche zugewiesen wurden. Das **Divider-Objekt** verwendet die Standardeigenschaftswerte des [**RecognizerContext-Objekts.**](inkrecognizercontext-class.md)

 

Das [**Divider-Objekt**](inkdivider-class.md) wendet den Erkennungskontext während der Layoutanalyse auf handschriftliche Elemente an. Alle Striche, die Sie dem Erkennungskontext direkt zuweisen, werden vom **Divider-Objekt** ignoriert. Weitere Informationen zur Texterkennung finden Sie unter Informationen zur [Handschrifterkennung.](about-handwriting-recognition.md)

 

 
