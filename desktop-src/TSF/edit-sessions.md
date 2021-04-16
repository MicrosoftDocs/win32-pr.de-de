---
title: Bearbeitungssitzungen
description: Wenn ein Text Dienst Text in einem Kontext abrufen, ändern oder festlegen muss, muss er eine Bearbeitungs Sitzung anfordern.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Text Dienst Framework (TSF), Bearbeitungs Sitzung
- TSF (Text Dienste-Framework), Sitzung bearbeiten
- Text Dienste, Sitzung bearbeiten
- Bearbeitungssitzung (edit session)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516052"
---
# <a name="edit-sessions"></a>Bearbeitungssitzungen

Wenn ein Text Dienst Text in einem Kontext abrufen, ändern oder festlegen muss, muss er eine *Bearbeitungs Sitzung* anfordern. Wenn eine Bearbeitungs Sitzung angefordert wird, aushandiert der TSF-Manager mit dem Besitzer des Ziel Kontexts für eine Dokument Sperre des angeforderten Typs. Wenn die Dokument Sperre erteilt wird, ermöglicht der TSF-Manager dem Text Dienst das Lesen und/oder Schreiben von Text in den oder aus dem Kontext.

 

 




