---
title: Hilfe (Eigenschaft)
description: Die Help-Eigenschaft stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309903"
---
# <a name="help-property"></a>Hilfe (Eigenschaft)

Die **Help** -Eigenschaft stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.

Die **Help** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)abgerufen.

Diese Eigenschaft enthält Informationen im Sprechblasen Format (wie in Quick Infos zu finden), das verwendet wird, um zu beschreiben, was das Objekt tut oder wie es verwendet wird. Beispielsweise kann die **Hilfe** Eigenschaft für eine Symbolleisten-Schaltfläche, die einen Drucker anzeigt, den folgenden Text enthalten: "druckt das aktuelle Dokument".

Der Text für die **Hilfe** Eigenschaft muss innerhalb der Benutzeroberfläche nicht eindeutig sein.

## <a name="when-to-support-the-help-property"></a>Unterstützung der Hilfe Eigenschaft

Server unterstützen die **Hilfe** Eigenschaft nicht, wenn andere Eigenschaften ausreichend Informationen zum Zweck des Objekts und zu den Aktionen bereitstellen, die das Objekt ausführt. Barrierefreie Objekte, die vom System bereitgestellte Steuerelemente verfügbar machen, unterstützen die **Hilfe** Eigenschaft nicht.

 

 




