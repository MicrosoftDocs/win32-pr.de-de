---
title: Status-Eigenschaft
description: Status-Eigenschaft
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402e88185e1024aa5958d06936a6529ae4012622
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341867"
---
# <a name="status-property"></a>Status-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Status des audioausgabekanals zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent * * *. Audiooutput. Status**



| Wert | BESCHREIBUNG                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | Der audioausgabechannel ist verfügbar (nicht ausgelastet).                                                                 |
| 1     | Die Audioausgabe wird nicht unterstützt. Dies ist beispielsweise der Fall, weil keine Soundkarte vorhanden ist.                                |
| 2     | Der audioausgabechannel kann nicht geöffnet werden (ist ausgelastet); beispielsweise, weil eine andere Anwendung Audiofunktionen wieder gibt. |
| 3     | Der audioausgabechannel ist ausgelastet, weil der Server die Benutzer Spracheingabe verarbeitet.                              |
| 4     | Der audioausgabechannel ist ausgelastet, weil zurzeit ein Zeichen spricht.                                       |
| 5     | Der audioausgabechannel ist nicht ausgelastet, aber er wartet auf die Benutzer Spracheingabe.                                    |
| 6     | Beim Versuch, auf den audioausgabechannel zuzugreifen, ist ein anderes (Unbekanntes) Problem aufgetreten.                          |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Mit dieser Einstellung kann Ihre Client Anwendung den audioausgabechannel Abfragen und einen ganzzahligen Wert zurückgeben, der den Status des audioausgabekanals angibt. Sie können dies verwenden, um zu bestimmen, ob es angemessen ist, das Zeichen zu verwenden, oder ob es sinnvoll ist, den Empfangsmodus zu aktivieren ( [**mithilfe der Abhör**](listen-method.md) Methode).

## <a name="see-also"></a>Weitere Informationen

[**Listencomplete-Ereignis**](listencomplete-event.md)


 

 




