---
description: Beschreibt die Strukturen, die von den Microsoft Direct3D 9-Video Schnittstellen verwendet werden.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Direct3D 9-Video Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346877"
---
# <a name="direct3d-9-video-structures"></a>Direct3D 9-Video Strukturen

Beschreibt die Strukturen, die von den Microsoft Direct3D 9-Video Schnittstellen verwendet werden.



| Struktur                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D \_ OMAC**](d3d-omac.md)<br/> Enthält einen Nachrichtenauthentifizierungscode (Mac).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> Enthält einen Initialisierungs Vektor (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ Konfigurieren von \_ Eingaben**](d3dauthenticatedchannel-configure-input.md)<br/> Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ Konfigurieren der \_ Ausgabe**](d3dauthenticatedchannel-configure-output.md)<br/> Enthält die Antwort auf einen aufzurufenden Befehl der [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) -Methode.<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL- \_ Konfiguration erneut initialisieren**](d3dauthenticatedchannel-configureinitialize.md)<br/> Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) -Befehl.<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ Konfigurieren von reprotection**](d3dauthenticatedchannel-configureprotection.md)<br/> Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ Protection**](d3dauthenticatedconfigure-protection.md) -Befehl.<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ Konfigurations Sitzung**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ CryptoSession**](d3dauthenticatedconfigure-cryptosession.md) -Befehl.<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL- \_ Konfiguration**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ SharedResource**](d3dauthenticatedconfigure-sharedresource.md) -Befehl.<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ Konfiguration reuncompressedencryption**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Enthält Eingabedaten für einen [**D3DAUTHENTICATEDCONFIGURE \_ -verschlüsselungszugreif**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) baren-Befehl.<br/>                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ - \_ Schutzflags**](d3dauthenticatedchannel-protection-flags.md)<br/> Gibt die Schutz Ebene für Videoinhalte an.<br/>                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md)<br/> Enthält Eingabedaten für die [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode.<br/>                                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Ausgabe**](d3dauthenticatedchannel-query-output.md)<br/> Enthält die Antwort auf einen aufzurufenden Befehl der [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) -Methode.<br/>                                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ querychanneltype- \_ Ausgabe**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ channelType**](d3dauthenticatedquery-channeltype.md) -Abfrage.<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Eingabe**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md) -Abfrage.<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Ausgabe**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ CryptoSession**](d3dauthenticatedquery-cryptosession.md) -Abfrage.<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ querydevicehandle- \_ Ausgabe**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ abvicehandle**](d3dauthenticatedquery-devicehandle.md) -Abfrage.<br/>                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Eingabe**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugangs-accessibleguid**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) -Abfrage.<br/>                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Ausgabe**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungszugriffbleguid**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) -Abfrage.<br/>                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguidcount- \_ Ausgabe**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ verschlüsselungsreferengen-accessibleguidcount**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) -Abfrage.<br/>                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ queryinfobustype- \_ Ausgabe**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ accessibilityattributabfrage**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Eingabe**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Enthält intput-Daten für eine [**D3DAUTHENTICATEDQUERY \_ OutputID**](d3dauthenticatedquery-outputid.md) -Abfrage.<br/>                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Ausgabe**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ OutputID**](d3dauthenticatedquery-outputid.md) -Abfrage.<br/>                                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Eingabe**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ outputidcount**](d3dauthenticatedquery-outputidcount.md) -Abfrage.<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Ausgabe**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ outputidcount**](d3dauthenticatedquery-outputidcount.md) -Abfrage.<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ queryprotection- \_ Ausgabe**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY- \_ Schutz**](d3dauthenticatedquery-protection.md) Abfrage.<br/>                                                                                                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Eingabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.<br/>                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.<br/>                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocesscount- \_ Ausgabe**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocesscount**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) -Abfrage.<br/>                 |
| [**D3DAUTHENTICATEDCHANNEL \_ queryuncompressedencryptionlevel- \_ Ausgabe**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. Accessible**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) -Abfrage.<br/>                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ queryunrestrictedprotectedsharedresourcecount- \_ Ausgabe**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) -Abfrage.<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Beschreibt die inhaltsschutzfunktionen eines Anzeige Treibers.<br/>                                                                                                                                                                                                                    |
| [**D3DENCRYPTED- \_ Block \_ Informationen**](d3dencrypted-block-info.md)<br/> Gibt an, welche Bytes in einer geschützten Video Oberfläche verschlüsselt werden.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Gibt die Hardware Überlagerungs Funktionen für ein Direct3D-Gerät an.<br/>                                                                                                                                                                                                                                            |
| [**Dxvabufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Gibt einen Puffer für die [**IDirect3DDXVADevice9:: Execute**](idirect3ddxvadevice9-execute.md) -Methode an.<br/>                                                                                                                                                                                                  |
| [**Dxvacompbufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Gibt die Anforderungen für komprimierte Oberflächen für die DirectX-Video Beschleunigung (DXVA) an.<br/>                                                                                                                                                                                                         |
| [**Dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Gibt die Dimensionen und das Pixel Format der nicht komprimierten Oberflächen für das Decodieren von DXVA-Videos an.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Video-APIs](direct3d-video-apis.md)
</dt> </dl>

 

 




