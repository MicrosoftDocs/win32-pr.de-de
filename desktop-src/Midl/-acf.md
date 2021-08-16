---
title: /acf-Switch
description: Mit dem Schalter /acf kann der Benutzer einen expliziten ACF-Dateinamen bereitstellen. Der Schalter ermöglicht auch die Verwendung verschiedener Schnittstellennamen in den IDL- und ACF-Dateien.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /acf switch MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37248ac346350f618eebc5ca81af144ecee91ce2acf40c39b9e980b574df4764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386127"
---
# <a name="acf-switch"></a>/acf-Switch

Mit dem Schalter **/acf** kann der Benutzer einen expliziten ACF-Dateinamen bereitstellen. Der Schalter ermöglicht auch die Verwendung verschiedener Schnittstellennamen in den IDL- und ACF-Dateien.

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*acf \_ filename* 
</dt> <dd>

Gibt den Namen des ACF an. Zwischen dem Schalter **/acf** und dem Dateinamen kann Leerraum vorhanden oder nicht vorhanden sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Standardmäßig erstellt der MIDL-Compiler den Namen des ACF, indem er die IDL-Dateinamenerweiterung (normalerweise .idl) durch .acf ersetzt. Wenn der Schalter **/acf** vorhanden ist, erhält der ACF seinen Namen aus dem angegebenen Dateinamen. Der Schalter **/acf** gilt nur für die IDL-Datei, die in der MIDL-Compilerbefehlszeile angegeben ist. Sie gilt nicht für importierte Dateien.

Wenn der Schalter **/acf** verwendet wird, muss der Schnittstellenname im ACF nicht mit dem MIDL-Schnittstellennamen übereinstimmen. Mit diesem Feature können Schnittstellen eine ACF-Spezifikation gemeinsam nutzen.

Wenn kein absoluter Pfad zu einem ACF angegeben ist, durchsucht der MIDL-Compiler das aktuelle Verzeichnis, die von der Option [**/I**](-i.md) bereitgestellten Verzeichnisse und die Verzeichnisse im INCLUDE-Pfad.

Wenn der ACF nicht gefunden wird, geht der MIDL-Compiler davon aus, dass für diese Schnittstelle kein ACF vorhanden ist. Weitere Informationen zur Sequenz von Verzeichnissen finden Sie in den Referenzeinträgen für die Schalter [**/I**](-i.md) und [**/no \_ def \_ idir.**](-no-def-idir.md) Weitere Informationen im Zusammenhang mit **/acf** finden Sie unter [Schnittstellendefinitionsdatei (IDL).](interface-definition-idl-file.md)

## <a name="examples"></a>Beispiele

**midl /acf bar.acf filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




