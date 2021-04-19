---
description: Die providetextdata-Methode wird von Mergemod.dll aufgerufen, um Textdaten aus dem Client Tool abzurufen. Mergemod.dll stellt den Namen aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: "\"Konfigurationsmodul. providetextdata\"-Methode (Mergemod. h)"
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370320"
---
# <a name="configuremoduleprovidetextdata-method"></a>"Konfigurationsmodul. providetextdata"-Methode

Die **providetextdata** -Methode wird von Mergemod.dll aufgerufen, um Textdaten aus dem Client Tool abzurufen. Mergemod.dll stellt den *Namen* aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.

Das Tool sollte S OK zurückgeben \_ und den entsprechenden Anpassungs Text in ConfigData bereitstellen. Das Client Tool ist für die Zuordnung der Daten zuständig, Mergemod.dllist jedoch für die Freigabe des Arbeitsspeichers zuständig. Dieses Argument muss ein **BSTR** -Objekt sein. **LPCWSTR** wird nicht akzeptiert.

Wenn das Tool keine Konfigurationsdaten für diesen *namens* Wert bereitstellt, sollte die Funktion "S false" zurückgeben \_ . In diesem Fall Mergemod.dll den Wert des Arguments ConfigData ignoriert und den Standardwert aus der Tabelle ModuleConfiguration verwendet.

Jeder andere Rückgabecode als s \_ OK oder s \_ false bewirkt, dass ein Fehler protokolliert wird (wenn ein Protokoll geöffnet ist), und führt zu einem Fehler beim Zusammenführen.

Da diese Funktion der standardmäßigen **BSTR** -Konvention folgt, entspricht NULL der leeren Zeichenfolge.

## <a name="syntax"></a>Syntax


```JScript
ConfigureModule.ProvideTextData(
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

Weitere Informationen finden Sie unter [**providebug TextData-Funktion**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




