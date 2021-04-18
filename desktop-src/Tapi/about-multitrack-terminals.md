---
description: Ein Multitrack-Terminal kann als Terminal angesehen werden, das eine Sammlung anderer Terminals ist. Jedes untergeordnete Terminal (a &\# 0034; Track&\# 0034;) kann ein Multitrack-Terminal oder ein Single-Track-Terminal sein.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Informationen zu Multitrack-Terminals
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358883"
---
# <a name="about-multitrack-terminals"></a>Informationen zu Multitrack-Terminals

Ein Multitrack-Terminal kann als Terminal angesehen werden, das eine Sammlung anderer Terminals ist. Jedes untergeordnete Terminal ("Track") kann ein Multitrack-Terminal oder ein Single-Track-Terminal sein.

Alle Multitrack-Terminals machen die [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) -Schnittstelle verfügbar, die generische Methoden zum Aufzählen, erstellen und Entfernen von Nachverfolgung-Terminals von einem Multitrack-Terminal umfasst. Alle Terminals, Single-Track und Multitrack, machen die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle verfügbar.

Ein Client, der über einen Zeiger auf eine [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle verfügt, kann ermitteln, ob das Terminal Multitrack oder Single-Track ist, indem das Terminal nach der [**itmultitrackterminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) -Schnittstelle abgefragt wird, die nur für Multitrack-Terminals verfügbar gemacht wird.

Das übergeordnete Terminal verwendet möglicherweise die [**itterminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) -Schnittstelle seiner Nachverfolgung-Terminals

Weitere Informationen finden Sie unter nach [Verfolgen von Terminals](track-terminals.md).

 

 
