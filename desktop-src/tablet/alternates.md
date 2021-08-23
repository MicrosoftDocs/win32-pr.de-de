---
description: Eine Alternative ist eine potenzielle Worterkennung für ein Erkennungssegment. Eine Recognizer generiert Alternativen und basiert auf akzeptablen Übereinstimmungen der Frei- oder Audioeingabe für ein Wörterbuch oder factoid.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternative Stile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76faf27b82a6bfc064fddbad3d2d4ca6c2dddc098d56bca340b677cea17a319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119337040"
---
# <a name="alternates"></a>Alternative Stile

Eine Alternative ist eine potenzielle Worterkennung für ein Erkennungssegment. Eine Recognizer generiert Alternativen und basiert auf akzeptablen Übereinstimmungen der Frei- oder Audioeingabe für ein Wörterbuch oder factoid.

> [!Note]  
> Die Konfidenzauswertung ist derzeit nur für die Microsoft English (USA) und Gestenerkennung verfügbar.

 

Manchmal kann die Ink-Datei mehrdeutige Unterschiede zwischen Segmenten haben. Die Recognizer vergleicht diese Segmente mit einem Recognizer-Wörterbuch, um mögliche Übereinstimmungen zu bestimmen. Wenn die Recognizer die Segmente vergleicht, verwaltet sie eine Liste möglicher alternativer Übereinstimmungen und weist jedem einen Konfidenzniveau zu, und es wird eine top-Auswahl getroffen.

> [!Note]  
> Die Erkennung kann keine Alternativen für einen Teil der Ink bereitstellen, der kleiner als ein Erkennungssegment ist.

 

 

 



