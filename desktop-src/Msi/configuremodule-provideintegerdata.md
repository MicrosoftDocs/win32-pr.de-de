---
description: Die ProvideIntegerData-Methode des ConfigureModule-Objekts wird von Mergemod.dll aufgerufen, um ganzzahlige Daten aus dem Clienttool abzurufen.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: ConfigureModule.ProvideIntegerData-Methode (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 96472a13902322d940dc7e756c3639f9befaf6764b3ede8521f27a885a50e8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143689"
---
# <a name="configuremoduleprovideintegerdata-method"></a>ConfigureModule.ProvideIntegerData-Methode

Die **ProvideIntegerData-Methode** des [**ConfigureModule-Objekts**](configuremodule-object.md) wird von Mergemod.dll, um ganzzahlige Daten aus dem Clienttool abzurufen.

Mergemod.dll gibt den *Namen aus* dem entsprechenden Eintrag in der [ModuleConfiguration-Tabelle an.](moduleconfiguration-table.md)

Das Tool sollte S OK zurückgeben \_ und die entsprechende Anpassungs-Ganzzahl in *ConfigData bereitstellen.*

Wenn das Tool keine Konfigurationsdaten für diesen *Name-Wert* enthält, sollte die Funktion S \_ FALSE zurückgeben. In diesem Fall Mergemod.dll den Wert des *ConfigData-Arguments* und verwendet den Standardwert aus der ModuleConfiguration-Tabelle.

## <a name="syntax"></a>Syntax


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Name des Elements, für das Daten abgerufen werden.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Zeiger auf Anpassungstext.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Client kann für jeden Datensatz in der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)nicht mehr als einmal aufgerufen werden. Beachten Sie, Mergemod.dll nicht mehrere Aufrufe an den Client für denselben "Name"-Wert. Wenn kein Datensatz in der Tabelle ModuleSubszugriff die -Eigenschaft verwendet, führt ein Eintrag in der ModuleConfiguration-Tabelle zu keinen Aufrufen des Clients.

### <a name="c"></a>C++

Weitere Informationen [**finden Sie unter ProvideIntegerData-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




