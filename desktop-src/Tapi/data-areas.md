---
description: Einige Telefon Sätze unterstützen das Konzept des Herunterladens von Daten aus dem oder Hochladen von Daten auf das Telefongerät, sodass das Telefon auf verschiedene Weise programmiert werden kann.
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: Datenbereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348602"
---
# <a name="data-areas"></a>Datenbereiche

Einige Telefon Sätze unterstützen das Konzept des Herunterladens von Daten aus dem oder Hochladen von Daten auf das Telefongerät, sodass das Telefon auf verschiedene Weise programmiert werden kann. TAPI modelliert diese Telefon Sätze als einen oder mehrere Download-und Uploadbereiche. Jeder Bereich wird durch eine Zahl zwischen 0 (null) und der Anzahl der auf dem Telefon verfügbaren Datenbereiche (minus 1) identifiziert. Die Größen der einzelnen Bereiche können variieren. Das Format der Daten selbst ist gerätespezifisch.

Die TAPI [**phonesetdata**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) -Funktion lädt einen Datenpuffer in einen bestimmten Datenbereich auf dem Telefongerät herunter, und die [**phonegetdata**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) -Funktion lädt den Inhalt eines bestimmten Datenbereichs auf dem Telefongerät in einen Puffer hoch.

Wenn ein Datenbereich eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendung gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

 

 



