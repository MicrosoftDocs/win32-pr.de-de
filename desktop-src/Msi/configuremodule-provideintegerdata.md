---
description: Die provideintegerdata-Methode des Objekts "konfiguriertmodule" wird von Mergemod.dll aufgerufen, um ganzzahlige Daten aus dem Client Tool abzurufen.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Konfigurations Methode. provideintegerdata-Methode (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364453"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Konfigurations Methode. provideintegerdata-Methode

Die **provideintegerdata** -Methode des [**Objekts "konfiguriertmodule**](configuremodule-object.md) " wird von Mergemod.dll aufgerufen, um ganzzahlige Daten aus dem Client Tool abzurufen.

Mergemod.dll stellt den *Namen* aus dem entsprechenden Eintrag in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)bereit.

Das Tool sollte S OK zurückgeben \_ und die passende Anpassungs Ganzzahl in *ConfigData* bereitstellen.

Wenn das Tool keine Konfigurationsdaten für diesen *namens* Wert bereitstellt, sollte die Funktion "S false" zurückgeben \_ . In diesem Fall Mergemod.dll den Wert des Arguments *ConfigData* ignoriert und den Standardwert aus der Tabelle ModuleConfiguration verwendet.

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

Der Name des Elements, für das Daten abgerufen werden.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Zeiger auf den Anpassungs Text.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Client kann für jeden Datensatz in der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" nicht mehr als einmal aufgerufen werden. Beachten Sie, dass Mergemod.dll für den gleichen "Name"-Wert nie mehrere Aufrufe an den Client sendet. Wenn kein Datensatz in der ModuleSubstitution-Tabelle die-Eigenschaft verwendet, bewirkt ein Eintrag in der ModuleConfiguration-Tabelle keine Aufrufe an den Client.

### <a name="c"></a>C++

Siehe [**provideintegerdata-Funktion**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




