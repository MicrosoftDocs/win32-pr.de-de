---
description: Die ccpsearch-Tabelle enthält die Liste der Datei Signaturen, die für das Kompatibilitäts Überprüfungs Programm (CCP) verwendet werden. Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.
ms.assetid: 98d21e24-1633-44b7-bfdb-5a40bab8d319
title: Ccpsearch-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368c0452fea011aca1080ca17020467ba6e0dc4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356678"
---
# <a name="ccpsearch-table"></a>Ccpsearch-Tabelle

Die ccpsearch-Tabelle enthält die Liste der Datei Signaturen, die für das Kompatibilitäts Überprüfungs Programm (CCP) verwendet werden. Mindestens eine dieser Dateien muss auf dem Computer eines Benutzers vorhanden sein, damit der Benutzer mit dem Programm konform ist.

Die ccpsearch-Tabelle weist die folgende Spalte auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="column"></a>Column

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Die Signatur \_ stellt eine eindeutige Datei Signatur dar und ist auch der externe Schlüssel in den Tabellen " [Signature](signature-table.md)", " [reglocator](reglocator-table.md)", " [inilocator](inilocator-table.md)", " [complocator](complocator-table.md)" und " [drlocator](drlocator-table.md) ".

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Auf diese Tabelle wird verwiesen, wenn die [ccpsearch-Aktion](ccpsearch-action.md) oder die [RMCCPSEARCH-Aktion](rmccpsearch-action.md) ausgeführt wird.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



