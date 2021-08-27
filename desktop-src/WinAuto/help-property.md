---
title: Help-Eigenschaft
description: Die Help-Eigenschaft stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6f8b226c483e3a3d68f878fccb940fc1a9f69f18b6fde62eed4b5a7a8ea9b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122190"
---
# <a name="help-property"></a>Help-Eigenschaft

Die **Help-Eigenschaft** stellt Informationen bereit, die den Benutzer über die Funktion eines Objekts informieren.

Die **Help-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)abgerufen.

Diese Eigenschaft enthält Informationen im Sprechblasenstil (wie in QuickInfos zu finden), die entweder verwendet werden, um zu beschreiben, was das Objekt tut oder wie es verwendet wird. Beispielsweise kann die **Hilfeeigenschaft** für eine Symbolleistenschaltfläche, die einen Drucker anzeigt, den folgenden Text bereitstellen: "Druckt das aktuelle Dokument."

Der Text für die **Help-Eigenschaft** muss innerhalb der Benutzeroberfläche nicht eindeutig sein.

## <a name="when-to-support-the-help-property"></a>Wann sollte die Hilfeeigenschaft unterstützt werden?

Server unterstützen die **Help-Eigenschaft** nicht, wenn andere Eigenschaften ausreichende Informationen zum Zweck des Objekts und zu den aktionen bereitstellen, die das Objekt ausführt. Barrierefreie Objekte, die vom System bereitgestellte Steuerelemente verfügbar machen, unterstützen die **Help-Eigenschaft** nicht.

 

 




