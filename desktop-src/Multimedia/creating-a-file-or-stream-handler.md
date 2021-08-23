---
title: Erstellen eines Datei- oder Streamhandlers
description: Erstellen eines Datei- oder Streamhandlers
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6732c572e390f3401f6e0472659bec7c522189b357b04d8ef7def20a7d9519b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785790"
---
# <a name="creating-a-file-or-stream-handler"></a>Erstellen eines Datei- oder Streamhandlers

In einer Anwendung, die in der Programmiersprache C geschrieben wurde, erstellt ein Datei- oder Streamhandler in der Regel eine Funktion für jede Methode. Ihre Anwendung greift über ein Array von Funktionszeigern, die der Streamhandler erstellt, auf diese Funktionen zu. Eine **IAVIStreamVtbl-Struktur** enthält das Array von Funktionszeigern. Ein Streamhandler kann einen beliebigen Namen zuweisen, der für die Methoden erstellt werden soll. Die Position des Funktionszeigers in der -Struktur impliziert die Entsprechung der Funktion mit der -Methode. Beispielsweise entspricht der erste Funktionszeiger in der -Struktur der **QueryInterface-Methode.** Ihr Streamhandler muss alle Funktionen einer Schnittstelle bereitstellen.

 

 




