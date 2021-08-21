---
title: SRStatus-Eigenschaft
description: SRStatus-Eigenschaft
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7cc079c79b3539fa5ad90da4f45907236f19d3b841cf580142446b230ff7c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975680"
---
# <a name="srstatus-property"></a>SRStatus-Eigenschaft

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob die Spracheingabe für das Zeichen gestartet werden kann.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). SRStatus_*



| Wert | BESCHREIBUNG                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Bedingungen unterstützen Spracheingaben.                                                                                                                                                                                                          |
| 1     | Auf diesem System ist kein Audioeingabegerät verfügbar. (Beachten Sie, dass dadurch nicht erkannt wird, ob ein Mikrofon installiert ist. Es kann nur erkannt werden, ob der Benutzer über eine ordnungsgemäß installierte eingabefähige Soundkarte mit einem funktionierenden Treiber verfügt.) |
| 2     | Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht ganz oben.                                                                                                                                           |
| 3     | Der Audioeingabe- oder -ausgabekanal ist derzeit ausgelastet, eine Anwendung verwendet Audio.                                                                                                                                                       |
| 4     | Beim Initialisieren des Spracherkennungssubsystems ist ein nicht angegebener Fehler aufgetreten. Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.                          |
| 5     | Der Benutzer hat die Spracheingabe in den erweiterten Zeichenoptionen deaktiviert.                                                                                                                                                                     |
| 6     | Fehler beim Überprüfen des Audiostatus, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gibt die Bedingungen zurück, die zur Unterstützung der Spracheingabe erforderlich sind, einschließlich des Status des Audiogeräts. Sie können diese Eigenschaft überprüfen, bevor Sie die [**Listen-Methode**](listen-method.md) aufrufen, um ihren Erfolg besser sicherzustellen.

Wenn die Spracheingabe im Eigenschaftenblatt des -Agents (Erweiterte Zeichenoptionen) aktiviert ist, lädt das Abfragen dieser Eigenschaft die zugeordnete Engine, sofern sie noch nicht geladen ist, und startet die Sprachdienste. Das heißt, der Überwachungsschlüssel ist verfügbar, und der Lauschtipp wird automatisch angezeigt. (Die Tasten "Lauschen" und "Lauschendes Tipp" sind nur aktiviert, wenn sie auch unter Erweiterte Zeichenoptionen aktiviert sind.) Wenn Sie jedoch die -Eigenschaft abfragen, wenn die Spracherkennung deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Listen-Methode**](listen-method.md)


 

 




