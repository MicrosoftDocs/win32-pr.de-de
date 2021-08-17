---
description: Einige Telefongruppen unterstützen das Herunterladen von Daten von oder das Hochladen von Daten auf das Telefongerät, wodurch das Telefonset auf unterschiedliche Weise programmiert werden kann.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Datenbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed05d6233a8c8ed31a2d00d28970a517ef181f00689c7da34673d3044fffb4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117946143"
---
# <a name="data-areas"></a>Datenbereiche

Einige Telefongruppen unterstützen das Herunterladen von Daten von oder das Hochladen von Daten auf das Telefongerät, wodurch das Telefonset auf unterschiedliche Weise programmiert werden kann. TAPI modelliert diese Telefonsätze so, als ob sie einen oder mehrere Download- oder Uploadbereiche haben. Jeder Bereich wird durch eine Zahl identifiziert, die von null bis zur Anzahl der auf dem Telefon verfügbaren Datenbereiche minus eins reicht. Die Größen der einzelnen Flächen können variieren. Das Format der Daten selbst ist gerätespezifisch.

Die [**phoneSetData-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) TAPI lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter, und die [**phoneGetData-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch.

Wenn ein Datenbereich eines Telefongeräts geändert wird, wird eine [**PHONE \_ STATE-Nachricht**](phone-state.md) an die Anwendung gesendet, um die Anwendung über die Zustandsänderung zu benachrichtigen. Parameter für diese Meldung geben einen Hinweis auf die Änderung an.

 

 



