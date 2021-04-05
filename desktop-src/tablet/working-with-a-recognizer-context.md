---
description: Das Divider-Objekt verwendet einen Erkennungs Kontext, um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Arbeiten mit einem erkentekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041809"
---
# <a name="working-with-a-recognizer-context"></a>Arbeiten mit einem erkentekontext

Das [**Divider**](inkdivider-class.md) -Objekt verwendet einen Erkennungs [**Kontext**](inkrecognizercontext-class.md) , um die Analyse der Erkennungs Segmente zu verbessern und Erkennungs Text für Handschrift Elemente zu generieren.

Sie können den Erkennungs Kontext festlegen, indem Sie die [**erkennzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft des [**Divider**](inkdivider-class.md) -Objekts verwenden oder den Erkennungs Kontext im Aufrufen des [Divider](/previous-versions/ms839465(v=msdn.10)) -Konstruktors (in verwaltetem Code) bereitstellen. Wenn ein Erkennungs Kontext für eine nicht Handschrifterkennung oder für eine Erkennung, die die freie Eingabe Funktion nicht unterstützt, der **erkennzercontext** -Eigenschaft zugewiesen wird, wird eine Ausnahme ausgelöst.

Wenn Erkenner nicht installiert sind oder ein Erkennungs Kontext nicht dem [**Divider**](inkdivider-class.md) -Objekt zugewiesen ist, verwendet das unter **Teiler** -Objekt keinen Erkennungs Kontext. In diesem Fall führt das layoutanalysefeature die Segment Division aus, und dem [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) -Objekt ist kein Text zugeordnet.

> [!Note]  
> Die [**erkenzercontext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) -Eigenschaft kann nicht geändert werden, nachdem dem [**Divider**](inkdivider-class.md) -Objekt Striche zugewiesen wurden. Das **Divider** -Objekt verwendet die Standardeigenschaftswerte des [**erkenzercontext**](inkrecognizercontext-class.md) -Objekts.

 

Das [**Divider**](inkdivider-class.md) -Objekt wendet den Erkennungs Kontext während der Layoutanalyse auf handgeschriebene Elemente an. Alle Striche, die Sie direkt dem Erkennungs Kontext zuweisen, werden vom **Divider** -Objekt ignoriert. Weitere Informationen zur Texterkennung finden Sie unter Informationen [zur Handschrifterkennung](about-handwriting-recognition.md).

 

 
