---
description: Eine Anwendung kann die RegSetValueEx-Funktion verwenden, um einen Wert und dessen Daten einem Schlüssel zuzuordnen. Eine Liste der von RegSetValueEx unterstützten Werttypen finden Sie unter Registrierungswerttypen.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Schreiben und Löschen von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd4e80dc3320d1af0931e111c82f473e0edf56ac071443397ffc3da0918f7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883992"
---
# <a name="writing-and-deleting-registry-data"></a>Schreiben und Löschen von Registrierungsdaten

Eine Anwendung kann die [**RegSetValueEx-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) verwenden, um einen Wert und dessen Daten einem Schlüssel zuzuordnen. Eine Liste der von **RegSetValueEx** unterstützten Werttypen finden Sie unter [Registrierungswerttypen.](registry-value-types.md)

Um einen Wert aus einem Schlüssel zu löschen, kann eine Anwendung die [**RegDeleteValue-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) verwenden. Um einen Schlüssel zu löschen, kann er die [**RegDeleteKey-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) verwenden. Ein gelöschter Schlüssel wird erst entfernt, wenn das letzte Handle für ihn geschlossen wurde. Unterschlüssel und Werte können nicht unter einem gelöschten Schlüssel erstellt werden.

Es ist nicht möglich, einen Registrierungsschlüssel während eines Schreibvorgangs zu sperren, um den Zugriff auf die Daten zu synchronisieren. Sie können jedoch den Zugriff auf einen Registrierungsschlüssel mithilfe von Sicherheitsattributen steuern. Weitere Informationen finden Sie unter Sicherheit und Zugriffsrechte für [Registrierungsschlüssel.](registry-key-security-and-access-rights.md)

Mehrere Registrierungsvorgänge können innerhalb einer einzelnen Transaktion ausgeführt werden. Um einer Transaktion einen Registrierungsschlüssel zuzuordnen, kann eine Anwendung die [**RegCreateKeyTransacted-**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) oder [**RegOpenKeyTransacted-Funktion**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) verwenden. Weitere Informationen zu Transaktionen finden Sie unter [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
