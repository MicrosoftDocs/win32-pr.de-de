---
description: Eine Anwendung kann die RegSetValueEx-Funktion verwenden, um einen Wert und seine Daten einem Schlüssel zuzuordnen. Eine Liste der Werttypen, die von RegSetValueEx unterstützt werden, finden Sie unter Registrierungs Werttypen.
ms.assetid: 75ac826a-f169-400c-b6d6-3e3ec9ebf996
title: Schreiben und Löschen von Registrierungsdaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5185c98f39a37512ec56fb994d5f1c4ba4b61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345029"
---
# <a name="writing-and-deleting-registry-data"></a>Schreiben und Löschen von Registrierungsdaten

Eine Anwendung kann die [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa) -Funktion verwenden, um einen Wert und seine Daten einem Schlüssel zuzuordnen. Eine Liste der Werttypen, die von **RegSetValueEx** unterstützt werden, finden Sie unter [Registrierungs Werttypen](registry-value-types.md).

Um einen Wert aus einem Schlüssel zu löschen, kann eine Anwendung die [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea) -Funktion verwenden. Um einen Schlüssel zu löschen, kann er die [**regdeletekey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya) -Funktion verwenden. Ein gelöschter Schlüssel wird erst entfernt, wenn das letzte Handle geschlossen wurde. Unterschlüssel und Werte können nicht unter einem gelöschten Schlüssel erstellt werden.

Es ist nicht möglich, einen Registrierungsschlüssel während eines Schreibvorgangs zu sperren, um den Zugriff auf die Daten zu synchronisieren. Sie können jedoch den Zugriff auf einen Registrierungsschlüssel mithilfe von Sicherheits Attributen steuern. Weitere Informationen finden Sie unter [Sicherheits-und Zugriffsrechte für den Registrierungsschlüssel](registry-key-security-and-access-rights.md).

Innerhalb einer einzelnen Transaktion können mehrere Registrierungs Vorgänge ausgeführt werden. Um einer Transaktion einen Registrierungsschlüssel zuzuordnen, kann eine Anwendung die [**regkreatekeytransfailed**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda) -oder [**regopenkeytransfailed**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda) -Funktion verwenden. Weitere Informationen zu Transaktionen finden Sie unter [Kerneltransaktions-Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal).

 

 
