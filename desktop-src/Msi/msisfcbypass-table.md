---
description: Die MsiSFCBypass-Tabelle enthält eine Liste von Dateien, die Windows Dateischutz umgehen sollten, wenn die Dateien auf Microsoft Windows Me installiert werden.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: MsiSFCBypass-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d233f09aa62b5f6d17112b1f5a98753e328f3a1746c452de5a5a1689a36f971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042670"
---
# <a name="msisfcbypass-table"></a>MsiSFCBypass-Tabelle

Die MsiSFCBypass-Tabelle enthält eine Liste von Dateien, die Windows Dateischutz umgehen sollten, wenn die Dateien auf Microsoft Windows Me installiert werden.

Die MsiSFCBypass-Tabelle weist die folgende Spalte auf.



| Spalte | Typ                         | Key | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Datei\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Der Fremdschlüssel für die [Dateitabelle,](file-table.md) der die Datei angibt, die Windows Dateischutz umgehen soll, wenn die Datei auf Windows Me installiert wird.

</dd> </dl>

 

 



