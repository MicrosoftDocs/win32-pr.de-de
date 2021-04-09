---
description: In der folgenden Tabelle werden die Zuordnungen zwischen Variant-Datentypen und OLE DB-Datentypen aufgelistet.
ms.assetid: 213458bf-b847-4ced-8a92-686b4eee6d07
title: Datentypzuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beae5a9ce1fbaafadfae54979d63c97310f57db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128552"
---
# <a name="data-type-mappings"></a>Datentypzuordnungen

In der folgenden Tabelle werden die Zuordnungen zwischen Variant-Datentypen und OLE DB-Datentypen aufgelistet.




| Variant-Datentyp | OLE DB-Datentyp |
|-------------------|------------------|
| VT \_ bool          | DbType \_ bool     |
| VT \_ BSTR          | DbType \_ BSTR     |
| VT- \_ ByRef         | DbType- \_ ByRef    |
| VT- \_ CY            | DbType- \_ CY       |
| VT- \_ Datum          | DbType- \_ Datum     |
| VT ( \_ dezimal)       | DbType \_ Decimal  |
| VT \_ leer         | DbType ist \_ leer.    |
| VT \_ FILETIME      | DbType \_ FILETIME |
| VT- \_ GUID          | DbType- \_ GUID     |
| VT \_ I1            | DbType \_ I1       |
| VT \_ I2            | DbType- \_ I2       |
| VT \_ I4            | DbType \_ I4       |
| VT \_ I8            | DbType \_ I8       |
| VT \_ null          | DbType \_ null     |
| VT \_ R4            | DbType \_ R4       |
| VT \_ R8            | DbType \_ UI8      |
| VT- \_ Vektor        | DbType- \_ Vektor   |
| VT \_ WSTR          | DbType \_ WSTR     |



 

In der folgenden Tabelle werden die Zuordnungen zwischen XML-Datentypen und OLE DB-Datentypen aufgelistet.



| Variant-Datentyp | OLE DB-Datentyp |
|-------------------|------------------|
| BIN. Base64        | DbType- \_ Bytes    |
| BIN. Dchen           | DbType \_ I8       |
| BOOLEAN           | DbType \_ bool     |
| CHAR              | DbType \_ Str      |
| DATE              | DbType- \_ Datum     |
| DATETIME          | DbType- \_ Datum     |
| DateTime. TZ       | DbType- \_ Datum     |
| Korrigiert. 14,4        | DbType \_ R4       |
| GLEITKOMMAZAHL             | DbType \_ R8       |
| I1                | DbType \_ I1       |
| I2                | DbType- \_ I2       |
| I4                | DbType \_ I4       |
| I8                | DbType \_ I8       |
| INT               | DbType \_ I8       |
| LONG              | DbType \_ I4       |
| NUMBER            | DbType \_ R8       |
| R4                | DbType \_ R4       |
| R8                | DbType \_ R8       |
| STRING            | DbType \_ WSTR     |
| TIME              | DbType \_ FILETIME |
| Zeit. TZ           | DbType \_ FILETIME |
| UI1               | DbType \_ UI2      |
| UI2               | DbType \_ UI2      |
| UI4               | DbType \_ UI4      |
| UI8               | DbType \_ UI8      |
| URI               | DbType \_ WSTR     |
| UUID              | DbType- \_ GUID     |



 

Zeichen folgen Daten können in andere Datentypen umgewandelt werden. Weitere Informationen finden Sie unter umwandeln [des Datentyps einer Spalte](-search-sql-castingdatacolumntype.md).

 

 



