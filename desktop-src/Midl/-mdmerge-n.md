---
title: /n-Schalter
description: Der/n-Schalter gibt die Kompositions Tiefe für das Verfassen von Metadatendateien an.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366860"
---
# <a name="n-switch"></a>/n-Schalter

Der **/n** -Schalter gibt die Kompositions Tiefe für das Verfassen von Metadatendateien an.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Namespace \_ Tiefe* 
</dt> <dd>

Gibt die Namespace Tiefe zum Verfassen in eine einzelne Metadatendatei an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im folgenden finden Sie die möglichen Werte Formate, die Sie mit dem **/n** -Schalter angeben können.



| Wertformat                   | BESCHREIBUNG                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Verfassen Sie alle Typen in der im Switch angegebenen Namespace Tiefe.               |
| -1                             | Erstellen Sie alle Typen in einer IDL-Datei pro Namespace.                              |
| <namespace>: Int32 > 0 | Verfassen Sie alle Typen mit einem entsprechenden Namespace in der im Switch angegebenen Tiefe. |
| <namespace>:-1           | Erstellen Sie alle Typen mit einem entsprechenden Namespace in eine Datei pro Namespace.          |



 

In der folgenden Tabelle werden die Ergebnisse aus verschiedenen Kombinationen des **/n** -Schalters angezeigt, die für diese Namespaces funktionieren.

-   Windows. Foundation. Collections. iiterable
-   Windows. UI. directui. Controls. Button
-   Windows. UI. directui. Controls. ListView
-   Windows. UI. immersive. Application. playto. Target
-   Windows. Web. Syndikation. RSS



| Switches                         | Ergebnis                                                                                                                                                                                                                                                       | Erklärung                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | Der letzte/n-Schalter überschreibt alle vorherigen – n-Switches.                                                                                                                                                                                                                                                                           |
| **/n:-1/n: Windows. UI: 2**         | <dl> <dt>Windows. Foundation. winmd</dt> <dt>Windows. UI. winmd</dt> <dt>Windows. Web. Syndikation. winmd</dt> </dl> | <dl> <dt>**Windows. Foundation** besteht immer aus – n:2</dt> <dt>**Windows. UI** -Typen werden gruppiert.</dt> <dt>" **Windows. Web. Syndikation** " wird unter "n:-1." erstellt.</dt> </dl>       |
| **/n: 1/n: Windows. UI. directui: 3** | <dl> Windows <dt>. Foundation. winmd</dt> Windows <dt>. UI. directui. winmd</dt> <dt>Windows. winmd</dt> </dl>       | <dl> <dt>**Windows. Foundation** besteht immer aus – n:2</dt> <dt>**Windows. UI. directui** ist auf Ebene 3 verfasst.</dt> <dt>Alle anderen Typen werden auf Ebene 1 zusammengesetzt.</dt> </dl> |



 

Hier sind die Regeln zum Verarbeiten mehrerer Instanzen des **/n** -Schalters aufgeführt.

-   Die spezifischere Instanz hat Vorrang. Wenn Sie z. b. **– n:a.b.c: 4 – n:a.b: 5** angeben, löst mdmerge A. b. c. D auf Ebene 4 auf, da a. b. c spezifischer als A.B. ist. A. b. E. F wird in Tiefe 5 aufgelöst, da es mit A. b übereinstimmt, nicht jedoch mit A.B.C.
-   Die letzte Instanz hat Vorrang. Wenn Sie z. b. **– n:5 – n:2** angeben, werden die Typen auf Ebene 2 zusammengesetzt.
-   Beide Regeln gelten. Wenn Sie – n:a.b.c: 4 – n:a.b.c: 1 angeben, wird der Namespace A. B. c auf Ebene 1 zusammengesetzt.

## <a name="examples"></a>Beispiele

**mdmerge.exe-Metadata \_ dir $ (SDK \_ - \_ Metadatenpfad)-i $ (interner \_ SDK- \_ \_ Metadatenpfad)-o $ (obj- \_ Pfad) \\ $O \\ systemmetadata-v-n:-1-n:Windows.Foundation: 2**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------|
| Client<br/> | Windows 8<br/>           |
| Server<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





