---
title: Erstellen einer Datei oder eines streamhandlers
description: Erstellen einer Datei oder eines streamhandlers
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036827"
---
# <a name="creating-a-file-or-stream-handler"></a>Erstellen einer Datei oder eines streamhandlers

In einer Anwendung, die in der Programmiersprache C geschrieben ist, erstellt ein Datei-oder streamhandler in der Regel eine Funktion für jede Methode. Die Anwendung greift auf diese Funktionen über ein Array von Funktions Zeigern zu, die der streamhandler erstellt. Eine **iavistreamvtbl** -Struktur enthält das Array von Funktions Zeigern. Ein Datenstrom Handler kann jeden beliebigen Namen zuweisen, den er für die Methoden erstellt. Die Position des Funktions Zeigers in der Struktur impliziert die Entsprechung der Funktion zur Methode. Beispielsweise entspricht der erste Funktionszeiger in der-Struktur der **QueryInterface** -Methode. Der Datenstrom Handler muss alle Funktionen einer Schnittstelle bereitstellen.

 

 




