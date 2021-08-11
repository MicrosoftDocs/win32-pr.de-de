---
title: Status-Eigenschaft
description: Status-Eigenschaft
ms.assetid: vs|msagent|~\pacontrol_8xd6.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edb1196e5ec41571c9c760b91a72b350b94f6b85f1f85af018691d3f25ecec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118245824"
---
# <a name="status-property"></a>Status-Eigenschaft

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt den Status des Audioausgabekanals zurück.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent**. AudioOutput.Status**



| Wert | BESCHREIBUNG                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 0     | Der Audioausgabekanal ist verfügbar (nicht ausgelastet).                                                                 |
| 1     | Die Audioausgabe wird nicht unterstützt. z. B. weil keine Soundkarte besteht.                                |
| 2     | Der Audioausgabekanal kann nicht geöffnet werden (ist ausgelastet). Zum Beispiel, weil eine andere Anwendung Audio abspielt. |
| 3     | Der Audioausgabekanal ist ausgelastet, da der Server Spracheingaben des Benutzers verarbeitet.                              |
| 4     | Der Audioausgabekanal ist ausgelastet, da derzeit ein Zeichen spricht.                                       |
| 5     | Der Audioausgabekanal ist nicht ausgelastet, wartet aber auf die Spracheingabe des Benutzers.                                    |
| 6     | Es gab ein anderes (unbekanntes) Problem beim Zugreifen auf den Audioausgabekanal.                          |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Mit dieser Einstellung kann Ihre Clientanwendung den Audioausgabekanal abfragen und einen Ganzzahlwert zurückgeben, der den Status des Audioausgabekanals angibt. Sie können damit bestimmen, ob es sinnvoll ist, das Zeichen sprechen zu lassen, oder ob es sinnvoll ist, den Lauschenmodus zu aktivieren (mithilfe der [**Listen-Methode).**](listen-method.md)

## <a name="see-also"></a>Weitere Informationen

[**ListenComplete-Ereignis**](listencomplete-event.md)


 

 




