---
description: Die FormatText-Methode des Record-Objekts formatiert Felder gemäß der Vorlage in Feld 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Record.FormatText-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 28170a4d92f656dcd12863eca5c003ccb851772f42de375e8f5f1b61a768ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626980"
---
# <a name="recordformattext-method"></a>Record.FormatText-Methode

Die **FormatText-Methode** des [**Record-Objekts**](record-object.md) formatiert Felder gemäß der Vorlage in Feld 0.

## <a name="syntax"></a>Syntax


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **FormatText-Methode** folgt der Funktionalität der [**MsiFormatRecord-Funktion,**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) wenn **MsiFormatRecord** ein NULL-Installerhandle als ersten Parameter übergeben wurde. Daher werden nur die Datensatzfeldparameter verarbeitet, und Eigenschaften stehen nicht für die Ersetzung zur Verfügung.

Beispielsweise wird eine Zeichenfolge wie "format this field: \[ 1 , format this property: property " in \] \[ \] "format this field: value from field 1, format this property: \[ property" aufgelöst. \]

Parameter, die [formatiert](formatted.md) werden sollen, werden in eckige Klammern \[ \] eingeschlossen... . Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach außen aufgelöst werden.

Wenn ein Teil der Zeichenfolge in geschweifte Klammern { } eingeschlossen ist und keine eckigen Klammern enthält, bleibt er unverändert, einschließlich der geschweiften Klammern.

Beachten Sie, dass **formatText** bei [benutzerdefinierten Aktionen](deferred-execution-custom-actions.md)mit verzögerter Ausführung nur einen begrenzten Satz von Eigenschaften unterstützt: die Eigenschaften CustomActionData und ProductCode. Weitere Informationen finden Sie unter [Abrufen von Kontextinformationen für benutzerdefinierte Aktionen mit verzögerter Ausführung.](obtaining-context-information-for-deferred-execution-custom-actions.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecord ist als 000C1093-0000-0000-C000-000000000046 definiert.<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Formatiert](formatted.md)
</dt> <dt>

[Spaltendatentypen](column-data-types.md)
</dt> </dl>

 

 




