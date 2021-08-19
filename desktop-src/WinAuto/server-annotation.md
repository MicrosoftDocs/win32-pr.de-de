---
title: Serveranmerkung
description: Dieser Abschnitt enthält Informationen zur Verwendung der Serveranmerkung.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9438184cf68d4a0f819afcd7e5497e627a0982e0f9fd9784c8a3460ab5121a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052538"
---
# <a name="server-annotation"></a>Serveranmerkung

Dieser Abschnitt enthält Informationen zur Verwendung der Serveranmerkung.

## <a name="summary"></a>Zusammenfassung

Sie definieren eine Klasse, die [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)implementiert, erstellen eine Instanz davon und teilen dem System mit, dass bestimmte Eigenschaften für bestimmte Benutzeroberflächenelemente überschrieben werden sollen. Wenn ein Client eine der Eigenschaften von einem der Benutzeroberflächenelemente anfing, wird Ihr -Objekt aufgerufen und erhält die Möglichkeit, einen Wert zur Verfügung zu stellen. Wenn Ihr -Objekt einen Wert zurückgibt, wird dieser Wert an den Client zurückgegeben. Wenn Ihr -Objekt keinen Wert zurück gibt, wird der Standardwert für dieses Benutzeroberflächenelement an den Client zurückgegeben.

## <a name="when-to-use-this-technique"></a>Einsatz dieser Technik

Verwenden Sie dieses Verfahren, wenn Sie die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für ein Objekt überschreiben möchten. Diese Technik ist viel einfacher als vorherige **IAccessible-Techniken.** Weitere Informationen finden Sie unter [Alternativen zu dynamischen Anmerkungen.](alternatives-to-dynamic-annotation.md)

Sie können die Serveranmerkung nicht verwenden, um die verfügbar gemachte Objektstruktur zu ändern. Um die Struktur eines Objekts zu ändern, müssen Sie einen vollständigen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren.

Weitere Informationen zur Serveranmerkung finden Sie in den folgenden Themen:

-   [Verwenden der Serveranmerkung](using-server-annotation.md)
-   [Beispiel für Serveranmerkungen](server-annotation-sample.md)

 

 




