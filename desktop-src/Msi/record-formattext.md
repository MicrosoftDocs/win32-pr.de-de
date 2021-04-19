---
description: Die formattext-Methode des Datensatz-Objekts formatiert Felder gemäß der Vorlage in Feld 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Record. formattext-Methode
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
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369179"
---
# <a name="recordformattext-method"></a>Record. formattext-Methode

Die **formattext** -Methode des [**Datensatz**](record-object.md) -Objekts formatiert Felder gemäß der Vorlage in Feld 0.

## <a name="syntax"></a>Syntax


```JScript
Record.FormatText()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **formattext** -Methode folgt der Funktion der [**msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) -Funktion, wenn **msiformatrecord** ein NULL-Installer-Handle als ersten Parameter übergeben wurde. Folglich werden nur die Parameter für das Daten Satz Feld verarbeitet, und die Eigenschaften sind nicht für die Ersetzung verfügbar.

Beispielsweise wird eine Zeichenfolge, z. b. "Formatieren dieses Felds: \[ 1 \] , Formatieren dieser Eigenschaft: \[ Eigenschaft \] " aufgelöst in "dieses Feld formatieren: Wert aus Feld 1. Formatieren Sie diese Eigenschaft: \[ Eigenschaft \] ."

Parameter, die [formatiert](formatted.md) werden sollen, werden in eckige Klammern eingeschlossen \[ ... \] . Die eckigen Klammern können iteriert werden, da die Ersetzungen von innen nach oben aufgelöst werden.

Wenn ein Teil der Zeichenfolge in geschweiften Klammern ({}) eingeschlossen ist und keine eckigen Klammern enthält, bleibt er unverändert, einschließlich der geschweiften Klammern.

Beachten Sie, dass **formattext** im Fall von [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)nur einen begrenzten Satz von Eigenschaften unterstützt: die Eigenschaften customaktiondata und ProductCode. Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iRecord ist definiert als 000c1093-0000-0000-C000-000000000046<br/>                                                                                                                                                                              |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msiformatrecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[Großformatige](formatted.md)
</dt> <dt>

[Spaltendatentypen](column-data-types.md)
</dt> </dl>

 

 




