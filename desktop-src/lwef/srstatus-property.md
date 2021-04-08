---
title: Srstatus (Eigenschaft)
description: Srstatus (Eigenschaft)
ms.assetid: 67618a35-05e4-4bb3-b910-c75de6e32578
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64cb6ba16bc024a52b65efa98c22fd089ad79da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037630"
---
# <a name="srstatus-property"></a>Srstatus (Eigenschaft)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**
</dt> <dd>

Gibt zurück, ob Spracheingaben für das Zeichen gestartet werden können.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**
</dt> <dd>

*Büros. ***Zeichen ("*** Merkmal-ID * * *"). Srstatus**



| Wert | BESCHREIBUNG                                                                                                                                                                                                                               |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Bedingungen unterstützen Spracheingaben.                                                                                                                                                                                                          |
| 1     | Auf diesem System ist kein Audioeingabegerät verfügbar. (Beachten Sie, dass hierdurch nicht erkannt wird, ob ein Mikrofon installiert ist. es kann nur erkennen, ob der Benutzer über eine ordnungsgemäß installierte Audiokarte mit einem funktionierenden Treiber verfügt.) |
| 2     | Ein anderer Client ist der aktive Client dieses Zeichens, oder das aktuelle Zeichen ist nicht oberstes Zeichen.                                                                                                                                           |
| 3     | Die Audioeingabe oder der Ausgabekanal ist derzeit ausgelastet, eine Anwendung verwendet Audiodaten.                                                                                                                                                       |
| 4     | Beim Initialisieren des sprach Erkennungs Subsystems ist ein nicht spezifizierter Fehler aufgetreten. Dies schließt die Möglichkeit ein, dass keine Sprach-Engine verfügbar ist, die der Spracheinstellung des Zeichens entspricht.                          |
| 5     | Der Benutzer hat die Spracheingabe in den erweiterten Zeichen Optionen deaktiviert.                                                                                                                                                                     |
| 6     | Beim Überprüfen des Audiostatus ist ein Fehler aufgetreten, aber die Ursache des Fehlers wurde vom System nicht zurückgegeben.                                                                                                                                |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft gibt die für die Unterstützung der Spracheingabe erforderlichen Bedingungen zurück, einschließlich des Status des Audiogeräts. Sie können diese Eigenschaft überprüfen, bevor Sie die Abhör Methode aufzurufen, [**um deren Erfolg**](listen-method.md) besser sicherzustellen.

Wenn Spracheingaben auf der Eigenschaften Seite des-Agents aktiviert sind (erweiterte Zeichen Optionen), wird beim Abfragen dieser Eigenschaft die zugeordnete Engine geladen, wenn Sie nicht bereits geladen ist, und Sprachdienste starten. Das heißt, der Abhör Schlüssel ist verfügbar, und der lauschabltip ist automatisch anzeigbar. (Der Abhör Schlüssel und der lauschtip sind nur aktiviert, wenn Sie auch in erweiterten Zeichen Optionen aktiviert sind.) Wenn Sie jedoch die-Eigenschaft Abfragen, wenn die Sprache deaktiviert ist, startet der Server die Sprachdienste nicht.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Abhör Methode**](listen-method.md)


 

 




