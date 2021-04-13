---
title: Antwortdateien
description: Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- Mittlerer l-compilermittell, Antwort Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd949a3704b0669fd37c5629307a59df9742010
ms.sourcegitcommit: ad8bd914e19508a67af232d8d59c0e0ee9c3948b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/07/2019
ms.locfileid: "104388833"
---
# <a name="response-files"></a>Antwortdateien

Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der Mittell-Compiler Antwort Dateien, die Schalter und Argumente enthalten. Eine Antwortdatei ist eine Textdatei, die eine oder mehrere Mittell-Compilerbefehlszeilenoptionen enthält. Im Gegensatz zu einer Befehlszeile ermöglicht eine Antwortdatei mehrere Zeilen von Optionen und Dateinamen. Dies kann aufgrund von Einschränkungen der Buildumgebung oder als benutzerfreundlicher Vorgang für Ihren Buildprozess nützlich sein. Sie können eine mittlerer l-Antwortdatei wie folgt angeben:

 **\@ Dateiname** für mittlere

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Gibt den Namen der Antwortdatei an. Der Antwort Dateiname muss unmittelbar auf das @-Zeichen folgen, ohne Leerzeichen zwischen dem @-Zeichen und dem Namen der Antwortdatei.

</dd> </dl>

Die Optionen in einer Antwortdatei werden so interpretiert, als würden Sie an dieser Stelle in der Befehlszeile der Mittell vorhanden sein. Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden. Sie können den umgekehrten Schrägstrich ( \) zum Verketten von Linien) nicht verwenden.

"Mittel l" unterstützt Befehlszeilenargumente, die eine oder mehrere Antwort Dateien enthalten, in Kombination mit anderen Befehls zeilenschaltern:

**Mittel l-Oicf @midl1.rsp -envwin32 @midl2.rsp ITF. idl**

Der mittlerer l-Compiler unterstützt keine netsted Response-Dateien.

 

 




