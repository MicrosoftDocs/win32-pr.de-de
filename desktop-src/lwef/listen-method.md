---
title: Listen-Methode
description: Listen-Methode
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc87a57d1ebdd3f36a2d56d85e0754f5005fd6c356fc9af98760bd0db90605f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748660"
---
# <a name="listen-method"></a>Listen-Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Aktiviert den Überwachungsmodus (Spracherkennung) für einen bestimmten Zeitraum.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters)*("**_CharacterID_*_"). Zustand "Lauschen"_ *  



| Teil    | Beschreibung                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Zustand* | Erforderlich. Ein boolescher Wert, der bestimmt, ob der Überwachungsmodus aktiviert oder deaktiviert werden soll. **True** Aktiviert den Überwachungsmodus. <br/> **False** Deaktiviert den Überwachungsmodus.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn Sie diese Methode auf **TRUE** festlegen, wird der Überwachungsmodus (aktiviert die Spracherkennung) für einen festgelegten Zeitraum (10 Sekunden) aktiviert. Obwohl Sie den Wert des Time outs nicht festlegen können, können Sie den Überwachungsmodus deaktivieren, bevor das Time out abläuft. Wenn Sie (oder ein anderer Client) erfolgreich den Überwachungsmodus auf festgelegt haben und versuchen, diese Eigenschaft auf **True** festzulegen, bevor das Time out abläuft, ist die Methode erfolgreich und setzt das Time out zurück. Wenn der Überwachungsmodus jedoch aktiviert ist, weil der Benutzer die Taste Lauschen drückt, ist die Methode erfolgreich, aber das Time out wird ignoriert, und der Überwachungsmodus endet basierend auf der Interaktion des Benutzers mit der Überwachungsschlüssel.

Diese Methode ist nur erfolgreich, wenn sie vom eingabeaktiven Client aufgerufen wird und die Sprachdienste gestartet wurden. Um sicherzustellen, dass die Sprachdienste gestartet wurden, fragen Sie [**srmodeID**](srmodeid-property.md) ab, oder legen Sie sie fest, oder legen Sie die [**Spracheinstellung**](voice-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object) fest, bevor Sie **Lauschen** aufrufen. Andernfalls schlägt die Methode fehl. Um den Erfolg dieser Methode zu erkennen, rufen Sie sie als Funktion auf und geben einen booleschen Wert zurück, der angibt, ob die Methode erfolgreich war.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



Die -Methode schlägt auch fehl, wenn der Benutzer die Abhörtaste drückt und Sie versuchen, **Lauschen** auf **False** festzulegen. Wenn der Benutzer jedoch die Überwachungsschlüssel losgelassen hat und kein Time out für den Überwachungsmodus aufgetreten ist, ist dies erfolgreich.

**Lauschen** schlägt auch fehl, wenn keine kompatible Sprach-Engine verfügbar ist, die der [**LanguageID-Einstellung**](languageid-property.md) des Zeichens entspricht, der Benutzer die Spracheingabe mithilfe des Microsoft-Agent-Eigenschaftenblatts deaktiviert hat oder das Audiogerät ausgelastet ist.

Wenn Sie diese Methode erfolgreich auf **True** festlegen, löst der Server das [**ListenStart-Ereignis**](listenstart-event.md) aus. Der Server sendet [**ListenComplete,**](listencomplete-event.md) wenn das Time out im Überwachungsmodus abgeschlossen ist oder Wenn Sie **Lauschen** auf **False** festlegen.

Diese Methode ruft nicht automatisch [**Stop auf**](stop-method.md) und gibt eine Überwachung zustandsanimation wieder, wie dies der Server beim Drücken der Lauschen-Taste tut. Dadurch können Sie ermitteln, ob die aktuelle Animation mithilfe der [**ListenStart-Animation**](listenstart-event.md) unterbrochen werden soll, indem **Sie Stop** aufrufen und Ihre eigene entsprechende Animation wiedergeben. Der Server ruft jedoch **Stop auf** und gibt eine Animation des Hörzustands wieder, wenn eine Benutzeräuhmung erkannt wird.

## <a name="see-also"></a>Weitere Informationen

[**LanguageID-Eigenschaft,**](languageid-property.md) [**ListenComplete-Ereignis,**](listencomplete-event.md) [**ListenStart-Ereignis**](listenstart-event.md)


 

