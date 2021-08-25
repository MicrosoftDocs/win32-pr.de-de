---
title: Antwortdateien
description: Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten.
ms.assetid: 53ee9ad2-1ab4-421f-99c9-66186da4bd9d
keywords:
- MIDL-Compiler MIDL, Antwortdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60a565c6178b3f671cccb391124297b07bb344c08d1cf7125ed26ba4f1b0704
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822110"
---
# <a name="response-files"></a>Antwortdateien

Als Alternative zum Platzieren aller Optionen in der Befehlszeile akzeptiert der MIDL-Compiler Antwortdateien, die Schalter und Argumente enthalten. Eine Antwortdatei ist eine Textdatei, die eine oder mehrere MIDL-Compilerbefehlszeilenoptionen enthält. Im Gegensatz zu einer Befehlszeile lässt eine Antwortdatei mehrere Zeilen mit Optionen und Dateinamen zu. Dies kann aufgrund von Einschränkungen Ihrer Buildumgebung oder zur Vereinfachung Ihres Buildprozesses nützlich sein. Sie können eine MIDL-Antwortdatei wie die folgende angeben:

**midl** **\@ filename**

<dl> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Gibt den Namen der Antwortdatei an. Der Name der Antwortdatei muss unmittelbar auf das @-Zeichen folgen, ohne Leerzeichen zwischen dem @-Zeichen und dem Namen der Antwortdatei.

</dd> </dl>

Optionen in einer Antwortdatei werden so interpretiert, als ob sie an dieser Stelle in der MIDL-Befehlszeile vorhanden sind. Jedes Argument in einer Antwortdatei muss in derselben Zeile beginnen und enden. Sie können den schrägen Schrägstrich ( ) nicht verwenden, \\ um Zeilen zu verketten.

MIDL unterstützt Befehlszeilenargumente, die eine oder mehrere Antwortdateien in Kombination mit anderen Befehlszeilenschaltern enthalten:

**midl -Oicf @midl1.rsp -envwin32 @midl2.rsp itf.idl**

Der MIDL-Compiler unterstützt keine geschachtelten Antwortdateien.

 

 




