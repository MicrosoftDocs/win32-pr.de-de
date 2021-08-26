---
title: MESSAGETABLE-Ressource
description: Definiert die ID und datei der Nachrichtentabellenressource einer Anwendung. Nachrichtentabellen sind spezielle Zeichenfolgenressourcen, die in der Ereignisprotokollierung und mit der FormatMessage-Funktion verwendet werden. Die Datei enthält eine vom Nachrichtencompiler generierte binäre Nachrichtentabelle MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- MESSAGETABLE-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378860e10ab6da929147e13a8120ee169204276e3c609b20176c22df9de15dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886720"
---
# <a name="messagetable-resource"></a>MESSAGETABLE-Ressource

Definiert die ID und datei der Nachrichtentabellenressource einer Anwendung. Nachrichtentabellen sind spezielle Zeichenfolgenressourcen, die in der Ereignisprotokollierung und mit der [**FormatMessage-Funktion**](/windows/desktop/api/winbase/nf-winbase-formatmessage) verwendet werden. Die Datei enthält eine vom Nachrichtencompiler generierte binäre Nachrichtentabelle MC.EXE.

Der Nachrichtencompiler generiert auch eine Ressourcenskriptdatei, die die **MESSAGETABLE-Anweisungen** enthält, die Sie zum Einschließen der Nachrichtentabellenressourcen in die kompilierte Ressourcendatei benötigen. Verwenden Sie die [**\# include-Direktive,**](-include.md) um dieses Ressourcenskript in Ihr Hauptressourcenskript einzufügen.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahlwert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Dateiname*
</dt> <dd>

Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine **MESSAGETABLE-Ressource** definiert:

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> </dl>

 

 