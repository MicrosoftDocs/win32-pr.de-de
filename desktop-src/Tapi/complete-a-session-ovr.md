---
description: Mit Abschluss Vorgängen kann eine Anwendung festlegen, wie eine Sitzung behandelt werden soll, wenn Faktoren wie z. b. ein ausgelasteter Ziel eine normale Verbindung verhindern.
ms.assetid: 71e61376-7913-42a9-a8e2-2ea6e4918f30
title: Sitzung beenden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5736b6be452413811f3530f44db280fe4e2a682f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345780"
---
# <a name="complete-a-session"></a>Sitzung beenden

Mit Abschluss Vorgängen kann eine Anwendung festlegen, wie eine Sitzung behandelt werden soll, wenn Faktoren wie z. b. ein ausgelasteter Ziel eine normale Verbindung verhindern.

Die [linecallcomplmode- \_ Konstanten](./linecallcomplmode--constants.md) definieren die möglichen Optionen, die eine Anwendung möglicherweise besitzt, je nach den Funktionen des Dienstanbieters.

Für eine bestimmte Adresse können zu einem beliebigen Zeitpunkt mehrere Anforderungen zum Abrufen von Anforderungen ausgegeben werden. Zum Identifizieren einzelner Anforderungen gibt die Implementierung einen [Vervollständigungs Bezeichner](completion-id-ovr.md)zurück. Wenn eine Anforderung zum Abschließen einer Anforderung in Bearbeitung abgebrochen wird, wird dieser Bezeichner für den Bezeichner verwendet

**TAPI 2. x:** Siehe [**linecompletecall,**](/windows/win32/api/tapi/nf-tapi-linecompletecall) [**lineuncompletecall.**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall)

**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol:: Connect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-connect), [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).

 

 
