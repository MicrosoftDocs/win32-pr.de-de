---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7fcfbf4aff25c1af0fbdb1f40471f6b54c4731f22fb2c736da42fe462eb390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750417"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Legt die Modus-ID des Für das Zeichen festgelegten Spracherkennungsmoduls fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

bszModeID

Die Modus-ID-Einstellung der Spracherkennungs-Engine für das Zeichen.

Diese Einstellung legt die Engine für die Spracheingabe eines Zeichens fest. Die Modus-ID für eine Spracherkennungs-Engine ist die vom Sprachanbieter definierte GUID, die den Modus der Engine eindeutig identifiziert (formatiert mit geschweiften Klammern und Bindestrichen). Weitere Informationen finden Sie in der [Dokumentation zum Microsoft Speech SDK.](https://msdn.microsoft.com/library/ee705648.aspx)

Wenn Sie eine Modus-ID angeben, die nicht mit der Spracheinstellung des Zeichens übereinstimmen, der Benutzer die Spracherkennung deaktiviert hat (auf dem Microsoft Agent-Eigenschaftenblatt) oder die Engine nicht installiert ist, ist dieser Aufruf nicht möglich. Wenn Sie keine Spracherkennungs-Engine-Modus-ID für das Zeichen festlegen, legt der Server eine id fest, die der Spracheinstellung des Zeichens entspricht (mithilfe von Microsoft Speech-API-Schnittstellen).

Wenn die Spracheingabe im Eigenschaftenblatt agent (Erweiterte Zeichenoptionen) aktiviert ist, wird durch Festlegen dieser Eigenschaft die zugeordnete Engine geladen (sofern sie noch nicht geladen ist) und die Spracherkennungsdienste gestartet. Das heißt, die Taste Lauschen ist verfügbar, und der Tipp zum Lauschen wird angezeigt. (Die Abhörtaste und der Tipp zum Lauschen sind nur aktiviert, wenn sie auch unter Erweiterte Zeichenoptionen aktiviert sind.) Wenn Sie jedoch die -Eigenschaft abfragen, wenn Sprache deaktiviert ist, startet der Server keine Spracherkennungsdienste.

Diese Eigenschaft gilt nur für den Client des Zeichens. Die Einstellung spiegelt nicht die Einstellung für andere Clients des Zeichens oder anderer Zeichen des Clients wider.

Die Anforderungen an die Sprach-Engine von Microsoft Agent basieren auf der Microsoft Speech-API. Engines, die die SAPI-Anforderungen von Microsoft Agent unterstützen, können mit dem -Agent installiert und verwendet werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




