---
title: Messagetable-Ressource
description: Definiert die ID und die Datei der Nachrichten Tabellen Ressource einer Anwendung. Nachrichten Tabellen sind spezielle Zeichen folgen Ressourcen, die bei der Ereignisprotokollierung und mit der FormatMessage-Funktion verwendet werden. Die Datei enthält eine binäre Nachrichten Tabelle, die vom Nachrichten Compiler generiert wurde, MC.EXE.
ms.assetid: c379cfff-23bf-4750-8d7a-d5c3c6783921
keywords:
- Messagetable-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- MESSAGETABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36281f7f6415465a6741f461574bca29c681cbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725552"
---
# <a name="messagetable-resource"></a>Messagetable-Ressource

Definiert die ID und die Datei der Nachrichten Tabellen Ressource einer Anwendung. Nachrichten Tabellen sind spezielle Zeichen folgen Ressourcen, die bei der Ereignisprotokollierung und mit der [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion verwendet werden. Die Datei enthält eine binäre Nachrichten Tabelle, die vom Nachrichten Compiler generiert wurde, MC.EXE.

Der Nachrichten Compiler generiert außerdem eine Ressourcen Skriptdatei, die die **messagetable** -Anweisungen enthält, die Sie zum Einschließen der Nachrichten Tabellen Ressourcen in die kompilierte Ressourcen Datei benötigen. Verwenden Sie die [**\# include**](-include.md) -Direktive, um dieses Ressourcen Skript in Ihr Hauptressourcen Skript einzubeziehen.

``` syntax
nameID MESSAGETABLE filename
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*
</dt> <dd>

Eindeutiger Name oder ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Ressource identifiziert.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Einfügen*
</dt> <dd>

Der Name der Datei, die die Ressource enthält. Der Name muss ein gültiger Dateiname sein. Es muss sich um einen vollständigen Pfad handeln, wenn sich die Datei nicht im aktuellen Arbeitsverzeichnis befindet.

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine **messagetable** -Ressource definiert:

``` syntax
1  MESSAGETABLE MSG00409.bin
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 