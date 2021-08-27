---
description: Mit Abschlussvorgängen kann eine Anwendung angeben, wie eine Sitzung behandelt werden soll, wenn Faktoren wie ein ausgelastetes Ziel eine normale Verbindung verhindern.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Abschließen einer Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20686f89feef5bb73d4ccbb786482f2528d700f42f0c4359fd965418077b8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118867978"
---
# <a name="complete-a-session"></a>Abschließen einer Sitzung

Mit Abschlussvorgängen kann eine Anwendung angeben, wie eine Sitzung behandelt werden soll, wenn Faktoren wie ein ausgelastetes Ziel eine normale Verbindung verhindern.

Die [ \_ LINECALLCOMPLMODE-Konstanten](./linecallcomplmode--constants.md) definieren die möglichen Optionen, die eine Anwendung abhängig von den Funktionen des Dienstanbieters haben kann.

Mehrere Aufrufabschlussanforderungen können für eine bestimmte Adresse gleichzeitig ausstehen. Um einzelne Anforderungen zu identifizieren, gibt die Implementierung einen [Abschlussbezeichner zurück.](completion-id-ovr.md) Beim Abbrechen einer Anforderung zur Anruferledigung wird auch dieser Bezeichner für die Anruferledigung verwendet.

**TAPI 2.x:** Siehe [**lineCompleteCall**](/windows/win32/api/tapi/nf-tapi-linecompletecall), [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall).

**TAPI 3.x:** Weitere [**Informationen finden Sie unter ITBasicCallControl::Verbinden**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**ITBasicCallControl::D isconnect.**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect)

 

 
