---
title: Abhör Methode
description: Abhör Methode
ms.assetid: ceb3b62f-2a33-4a13-b608-4cfa800be38a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813fb155074c4cc47a51ec7241eddd332edbcc3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038861"
---
# <a name="listen-method"></a>Abhör Methode

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Schaltet den Empfangsmodus (Spracherkennung) für einen zeitgesteuerten Zeitraum ein.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Agent. ***Zeichen * * * * ("*** Merkmal-ID * * *").* *  *Status* lauschen



| Teil    | Beschreibung                                                                                                                                                                      |
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Zustand* | Erforderlich. Ein boolescher Wert, der bestimmt, ob der Empfangsmodus aktiviert oder deaktiviert werden soll. **True** Schaltet den Modus für die Überwachung ein. <br/> **False** Schaltet den Lesemodus aus.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn diese Methode auf **true** festgelegt wird, wird der Empfangsmodus (aktiviert die Spracherkennung) für einen festgelegten Zeitraum (10 Sekunden) aktiviert. Obwohl Sie den Wert für das Timeout nicht festlegen können, können Sie den Empfangsmodus deaktivieren, bevor das Timeout abläuft. Wenn Sie (oder ein anderer Client) den Empfangsmodus für erfolgreich festgelegt haben und Sie versuchen, diese Eigenschaft vor Ablauf des Timeouts auf **true** festzulegen, wird die Methode erfolgreich ausgeführt, und das Timeout wird zurückgesetzt. Wenn der Überwachungsmodus jedoch auf ON eingestellt ist, da der Benutzer die Abhör Taste drückt, wird die Methode erfolgreich ausgeführt, aber das Timeout wird ignoriert, und der Empfangsmodus wird basierend auf der Interaktion des Benutzers mit dem lauschenden Schlüssel beendet.

Diese Methode ist nur erfolgreich, wenn Sie vom Eingabe aktiven Client aufgerufen wird und die Sprachdienste gestartet wurden. Um sicherzustellen, dass Sprachdienste gestartet wurden, Fragen Sie die [**srmodeid**](srmodeid-property.md) ab, oder legen Sie Sie fest, oder legen Sie die [**sprach**](voice-property.md) Einstellung für einen [**Befehl**](/windows/desktop/lwef/the-command-object) fest, bevor Sie **lauschen** Um den Erfolg dieser Methode zu erkennen, nennen Sie Sie als Funktion, und Sie gibt einen booleschen Wert zurück, der angibt, ob die Methode erfolgreich ausgeführt wurde.


```
   If Genie.Listen(True) Then
      'The method succeeded

   Else
      ' The method failed

   End If
```



Die-Methode schlägt auch fehl, wenn der Benutzer die Abhör Taste drückt, und Sie versuchen, das **lauschen** auf **false** festzulegen. Wenn der Benutzer jedoch keinen Timeout für den abhörenden Schlüssel hat und kein Timeout aufgetreten ist, wird er erfolgreich ausgeführt.

**Lauschen** schlägt auch fehl, wenn keine kompatible Sprach-Engine verfügbar ist, die mit der [**LanguageID**](languageid-property.md) -Einstellung des Zeichens übereinstimmt, der Benutzer die Spracheingabe mithilfe der Eigenschaften Seite "Microsoft-Agent" deaktiviert hat oder das Audiogerät ausgelastet ist.

Wenn Sie diese Methode erfolgreich auf **true** festgelegt haben, löst der Server das [**ListenStart**](listenstart-event.md) -Ereignis aus. Der Server sendet [**listencomplete**](listencomplete-event.md) , wenn das Timeout für den Lesemodus abgeschlossen ist, oder wenn Sie **lauschen** auf **false** festlegen.

Diese Methode ruft nicht automatisch " [**Beenden**](stop-method.md) " auf und wiedergeben eine Animation zum lauschen des Zustands, wenn der Server beim Drücken der Abhör Taste gedrückt wird. Auf diese Weise können Sie bestimmen, ob die aktuelle Animation mithilfe der [**ListenStart**](listenstart-event.md) -Animation unterbrechen werden soll, indem Sie " **stoppen** " aufrufen und ihre eigene passende Animation wiedergeben Der Server ruft jedoch " **Beenden** " auf und spielt eine Animation für den hörzustand, wenn eine Benutzer Äußerung erkannt wird.

## <a name="see-also"></a>Weitere Informationen

[**LanguageID-Eigenschaft**](languageid-property.md), [**listencomplete-Ereignis**](listencomplete-event.md), [**ListenStart-Ereignis**](listenstart-event.md)


 

