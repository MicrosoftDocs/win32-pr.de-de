---
title: /ACF-Schalter
description: Mit dem Schalter/ACF kann der Benutzer einen expliziten ACF-Dateinamen angeben. Der Switch ermöglicht außerdem die Verwendung verschiedener Schnittstellennamen in den IDL-und ACF-Dateien.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948241"
---
# <a name="acf-switch"></a>/ACF-Schalter

Mit dem Schalter **/ACF** kann der Benutzer einen expliziten ACF-Dateinamen angeben. Der Switch ermöglicht außerdem die Verwendung verschiedener Schnittstellennamen in den IDL-und ACF-Dateien.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*ACF \_ Dateiname* 
</dt> <dd>

Gibt den Namen der ACF an. Zwischen dem **/ACF** -Switch und dem Dateinamen kann ein Leerzeichen stehen oder nicht vorhanden sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Standardmäßig erstellt der-compilercompiler den Namen der ACF, indem er die IDL-Dateinamenerweiterung (i. d. d. idl) durch. ACF ersetzt. Wenn der **/ACF** -Schalter vorhanden ist, nimmt die ACF den Namen des angegebenen Datei namens an. Der **/ACF** -Schalter gilt nur für die IDL-Datei, die in der Befehlszeile des compl-Compilers angegeben ist. Es gilt nicht für importierte Dateien.

Wenn der **/ACF** -Schalter verwendet wird, muss der Schnittstellen Name in der ACF nicht mit dem Namen der Mittell-Schnittstelle identisch sein. Diese Funktion ermöglicht es Schnittstellen, eine ACF-Spezifikation gemeinsam zu nutzen.

Wenn kein absoluter Pfad zu einer ACF angegeben ist, sucht der Mittelwert Compiler im aktuellen Verzeichnis, den Verzeichnissen, die von der [**/I**](-i.md) -Option bereitgestellt werden, und den Verzeichnissen im Include-Pfad.

Wenn die ACF nicht gefunden wird, geht der Mittelwert Compiler davon aus, dass für diese Schnittstelle keine ACF vorhanden ist. Weitere Informationen zur Reihenfolge der Verzeichnisse finden Sie in den Verweis Einträgen für die Schalter [**/I**](-i.md) und [**/No \_ DEF \_ Idir**](-no-def-idir.md) . Weitere Informationen zu **/ACF** finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Beispiele

**Mittel l/ACF Bar. ACF Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/No \_ DEF \_ Idir**](-no-def-idir.md)
</dt> </dl>

 

 




