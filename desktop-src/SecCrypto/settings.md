---
description: Wird zum Konfigurieren von CAPICOM-Komponenten verwendet.
title: Einstellungs Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372149"
---
# <a name="settings-object-cryptography"></a>Einstellungs Objekt (Kryptografie)

\[Das **Einstellungs** Objekt ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Das **Einstellungs** Objekt wird verwendet, um CAPICOM-Komponenten zu konfigurieren.

## <a name="members"></a>Member

Das **Einstellungs** Objekt verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Einstellungs** Objekt verfügt über diese Eigenschaften.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Eigenschaft</th>
<th style="text-align: left;">Zugriffstyp</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>Activedirectoriysearchlocation</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Legt den Active Directory Suchspeicherort fest oder ruft ihn ab. Der ursprüngliche Speicherort ist standardmäßig nicht angegeben. Wenn der Speicherort nicht angegeben ist, wird der globale Katalog durchsucht, und die Standard Domäne wird durchsucht. Die Suche bestimmt, ob das Attribut des Benutzer Zertifikats an diesem Speicherort veröffentlicht wird.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>Enablepromptforcertifiereui</strong></a><br/></td>
<td style="text-align: left;">Lesen/Schreiben<br/></td>
<td style="text-align: left;">Legt einen booleschen Wert fest, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können, oder ruft ihn ab. <br/>
<blockquote>
[!Note]<br />
Wenn Sie diese Eigenschaft festlegen, werden Warnungen nicht deaktiviert, die generiert werden, bevor die Verwendung von privaten Schlüsseln aus einer webbasierten Anwendung erfolgt.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Das **Einstellungs** Objekt kann erstellt werden und ist für die Skripterstellung sicher. Die ProgID für das **Einstellungs** Objekt ist "CAPICOM". Einstellungen. 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kryptografieobjekte**](cryptography-objects.md)
</dt> </dl>

 

 




