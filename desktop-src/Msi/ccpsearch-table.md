---
description: Die TABELLE ANTIVIRUSSearch enthält die Liste der Dateisignaturen, die für das Compliance Checking Program (ANTIVIRUS) verwendet werden. Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: TABELLESuchen einer Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d20894960dce7f346601bd2ed459140caa305323ca02d14d54416f32737216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821840"
---
# <a name="ccpsearch-table"></a>TABELLESuchen einer Tabelle

Die TABELLE ANTIVIRUSSearch enthält die Liste der Dateisignaturen, die für das Compliance Checking Program (ANTIVIRUS) verwendet werden. Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.

Die TABELLE TONTSearch enthält die folgende Spalte.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatur\_
</dt> <dd>

Die Signatur stellt eine eindeutige Dateisignatur dar und ist auch der externe Schlüssel in den \_ [Tabellen Signature,](signature-table.md) [RegLocator,](reglocator-table.md) [IniLocator,](inilocator-table.md) [CompLocator](complocator-table.md)und [DrLocator.](drlocator-table.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Auf diese Tabelle wird verwiesen, wenn die [AKTION FLOCKSearch](ccpsearch-action.md) oder [RMCCPSearch](rmccpsearch-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



