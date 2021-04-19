---
description: Die Export-Methode des Datenbankobjekts kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine Textarchiv Datei.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Database. Export-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370025"
---
# <a name="databaseexport-method"></a>Database. Export-Methode

Die **Export** -Methode des [**Daten Bank**](database-object.md) Objekts kopiert die Struktur und die Daten aus einer angegebenen Tabelle in eine [Textarchiv Datei](text-archive-files.md).

## <a name="syntax"></a>Syntax


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tabelle* 
</dt> <dd>

Der erforderliche Name der Datenbanktabelle. Unterscheidung nach Groß-/Kleinschreibung bei Verwendung der Installer-Datenbank

</dd> <dt>

*path* 
</dt> <dd>

Erforderliche Zeichenfolge, die der Pfad zu dem Ordner ist, in dem die Textdatei abgelegt wird.

</dd> <dt>

*datei* 
</dt> <dd>

Der erforderliche Name der zu erstellenden Datei. Dies schließt den Ordner nicht ein, da dieser im Path-Objekt festgelegt werden muss.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




