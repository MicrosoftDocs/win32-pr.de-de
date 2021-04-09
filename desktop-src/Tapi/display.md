---
description: TAPI bietet Zugriff auf die Anzeige von Smartphones.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129308"
---
# <a name="display"></a>Anzeige

TAPI bietet Zugriff auf die Anzeige eines Telefons. Die Anzeige wird als alphanumerischer Bereich mit Zeilen und Spalten modelliert. Die Gerätefunktionen eines Telefons geben die Größe der Anzeige eines Telefons als Anzahl von Zeilen und die Anzahl der Spalten an. Beide Zahlen sind 0 (null), wenn auf dem Telefongerät keine Anzeige vorhanden ist. Verwenden Sie " [**phonesetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) ", um Informationen in die Anzeige eines geöffneten Telefon Geräts zu schreiben, und [**phonegetdisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) , um den aktuellen Inhalt der Anzeige eines Telefons abzurufen.

Wenn die Anzeige eines Telefon Geräts geändert wird, wird eine [**Telefon \_ Zustands**](phone-state.md) Meldung an die Anwendungsfunktion gesendet, um die Anwendung über die Statusänderung zu benachrichtigen. Die Parameter für diese Nachricht geben Aufschluss über die Änderung.

 

 



