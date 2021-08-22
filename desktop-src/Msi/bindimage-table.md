---
description: Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder DLL, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: BindImage-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae4f36f3b258845bcba13748495dc9dfb53c86268bd61e98475d1c7c0c282
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500765"
---
# <a name="bindimage-table"></a>BindImage-Tabelle

Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder DLL, die an die von ihr importierten DLLs gebunden werden muss.

Die BindImage-Tabelle enthält die folgenden Spalten.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Datei\_ | [Identifier](identifier.md) | J   | N        |
| Pfad   | [Paths](paths.md)           | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Ein externer Schlüssel für die Spalte eine der [Dateitabellen](file-table.md). Dies muss eine ausführbare Datei oder eine DLL-Datei sein.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Pfad
</dt> <dd>

Eine durch Semikolons getrennte Liste von Pfaden, die die zu durchsuchenden Pfade darstellen, um die importierten DLLs zu finden. Die Liste ist normalerweise eine Liste von Eigenschaften, bei der jede Eigenschaft in eckige Klammern \[ \] () eingeschlossen ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Installationsprogramm berechnet die virtuelle Adresse jeder Funktion, die aus allen DLLs importiert wird, und die berechnete virtuelle Adresse wird dann in der Import Address Table (IAT) des importierenden Images gespeichert.

Auf diese Tabelle wird verwiesen, wenn die [BindImage-Aktion](bindimage-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



